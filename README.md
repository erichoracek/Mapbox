Mirrors [mapbox-gl-native](https://github.com/mapbox/mapbox-gl-native) using [Rome](https://github.com/neonichu/Rome) to create a Carthage-compatible Xcode project.

To update to a new version:

- Update the Pod:
```
$ bundle update
$ bundle exec pod update
```
- Remove the current shared scheme
```
$ rm -rf Pods/Pods.xcodeproj/xcshareddata
```
- Share the scheme that builds `Mapbox.framework` in `Pods.xcodeproj`
- Archive the framework using Carthage:
```
$ carthage build --no-skip-current
$ carthage archive Mapbox
```
