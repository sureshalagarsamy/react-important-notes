### Difference between `useMemo` and `useCallback` in react

`useMemo` and `useCallback` use memoization.

Both `useMemo` and `useCallback` remember something between renders until the dependencies change.

The difference is just what they **remember**.

`useMemo` will **remember** the returned value from the function

`useCallback` will **remember** the actual function
