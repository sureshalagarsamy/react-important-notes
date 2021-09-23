### Difference between `useMemo` and `useCallback` in react

`useMemo` and `useCallback` use memoization.

Both `useMemo` and `useCallback` remember something between renders until the dependencies change.

The difference is just what they **remember**.

`useMemo` will **remember** the returned value from the function

`useCallback` will **remember** the actual function

### Change detection in Angular and React

React and Angular change detections are different. But they are common in one important thing. Making a difference of `previous` and `current` state from `memory` (not from DOM) and rendering only what has been changed. 

##### In Angular

* change detection is triggerd by `zone.js` at the end of the `each callstack`
* Change detection `starts from the root component` and it goes down through the components tree
* Traversing components tree, it checks which values in component templates need to be updated and updates the DOM.

##### In React

* Change detection is not triggered after callbacks of `async` actions. It’s triggered by calling method `setState` on component.
* Change detection starts `not from the root component`, but from component in which `setState` was called.
*  in React we have class `React.PureComponent`. We can use this class to avoid unnecessary change detection.
