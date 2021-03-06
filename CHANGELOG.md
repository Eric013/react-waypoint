## master (unreleased)

## 4.1.0

- Add `horizontal` prop. Use it to make the waypoint trigger on horizontal scrolling.

## 4.0.4

- Delay initial calling of handleScroll when mounting.

## 4.0.3

- Extract event listener code to consolidated-events package.

## 4.0.2

- Prevent event listeners from leaking.

## 4.0.1

- Fix error when a waypoint unmounts another waypoint as part of handling a
  (scroll/resize) event.

## 4.0.0

- [Breaking] Use passive event listeners in browsers that support them. This
  will break any Waypoint event handler that was calling
  `event.preventDefault()`.
- Initialize fewer event listeners.

## 3.1.3

- Avoid warnings from React about calling PropTypes directly (#119).

## 3.1.2

This version contains a fix for errors of the following kind:

```
Unable to get property 'getBoundingClientRect' of undefined or null reference
```

## 3.1.1

- Fix passing props to super class, to make react-waypoint compatible with [preact](https://github.com/developit/preact) (thanks @kamotos!)

## 3.1.0

New properties have been added to the `onEnter`/`onLeave`/`onPositionChange`
callbacks:

- `waypointTop` - the waypoint's distance to the top of the viewport.
- `viewportTop` - the distance from the scrollable ancestor to the viewport top.
- `viewportBottom` - the distance from the bottom of the scrollable ancestor to
  the viewport top.

## 3.0.0

- Change `threshold` to `bottomOffset` and `topOffset`
- Add `throttleHandler` prop to allow scrolling to be throttled

## 2.0.3

- Added `debug` prop

## 2.0.2

- Improved position calculation

## 2.0.1

- Add React 15 support

## 2.0.0

- Breaking: Unify arguments passed to callbacks
- Add `displayName`

## 1.3.1

- Handle invisible waypoint parents
- Add `onPositionChange`

## 1.3.0

- Rename `scrollableParent` prop to `scrollableAncestor`

## 1.2.3

- Simplify `getWindow` usage
- Allow any `scrollableParent`

## 1.2.2

- Add `fireOnRapidScroll` prop

## 1.2.1

- Make bundled waypoint.js easier to import

## 1.2.0

- Upgrade Babel from 5 to 6
- Convert from CommonJS to ES2015 modules
- Convert from React.createClass to ES2015 class
- Remove bower support

## 1.1.3

- Calculate proper offset when <html> or <body> has a margin

## 1.1.2

- Fix built version

## 1.1.1

- Add statics for edge argument used by `onEnter` and `onLeave`
- Prevent scroll handler from blowing up if the component is not mounted at the
  time of execution

## 1.1.0

- Add second parameter to `onEnter` and `onLeave` callbacks to indicate
  from which direction the waypoint entered _from_ and _to_ respectively

## 1.0.6

- Prevent duplicate onError/onLeave callbacks

## 1.0.5

- Prevent error when `<html>` has a scrollable overflow styling

## 1.0.4

- Bump `react` dependency to 0.14 and add `react-dom` to `peerDependencies`

## 1.0.3

- Replace `this.getDOMNode()` with `React.findDOMNode(this)`
- Improve support for scrolling very quickly

## 1.0.2

- Add event object and scope to onEnter/onLeave calls
- Allow React 0.14.0-beta peerDependency
- Always remove window resize event listener

## 1.0.1

- Ignore more files for bower and npm packages
- Commit the built version for bower package

## 1.0.0

- Add 'jsx' syntax to the unbuilt version of the component, and build into
  'build/ReactWaypoint.js' with webpack.
- Fix corner case where scrollable parent is not the window and the window
  resize should trigger a Waypoint callback.

## 0.3.0

- Fix Waypoints with the window element as their scrollable parent (Firefox
  only)

## 0.2.0

- Fix Waypoints with the window element as their scrollable parent
- Change default threshold from 0.1 to 0
- Guard against undefined scrollable parent when unmounting

## 0.1.0

- Initial release
