Add your answers to the Algorithms exercises here.

```
a)  a = 0
    while (a < n * n * n):==> O(n)
      a = a + n * n ========> O(1)
```

`This is O(n) because every time n is incresed the run time grows.`

```

b)  sum = 0
    for i in range(n): =======================> O(n)
      i += 1 =================================> O(1)
      for j in range(i + 1, n): ==============> O(n)
        j += 1 ===============================> O(1)
        for k in range(j + 1, n): ============> O(n)
          k += 1 =============================> O(1)
          for l in range(k + 1, 10 + k): =====> O(n)
            l += 1 ===========================> O(1)
            sum += 1 =========================> O(1)
```

`The run time for this is O(n^3) because k is a set number in the L loop and will never change it will loop 10 time no matter what.`

```
c)  def bunnyEars(bunnies):=================> O(1)
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1) ======> O(n)
```

`The run time complexity is O(n) because the return will take place every time n is greater that 2.`

```

Suppose that you have an _n_-story building and plenty of eggs. Suppose also that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get broken if dropped off a floor less than floor _f_. Devise a strategy to determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the runtime complexity of your solution.
```

`If I needed to find the floor where the egg did not break then I would start in the middle floor of the building. If the egg broke then I could eliminate all of the floors above me.` `I would then split the lower half of the floors and move to the middle of them.`
`if the egg did not break then I can get rid of all of the floors below me. I would repete this process until I found the right floor.` ======= Run Time Complexity is ====> O(logn)
because no matter how much n was increased the time would not get much larger.
