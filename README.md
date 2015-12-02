Mirrors [mapbox-gl-native](https://github.com/mapbox/mapbox-gl-native) using [Rome](https://github.com/neonichu/Rome) to create a Carthage-compatible Xcode project.

### To install:

- Add `github "erichoracek/Mapbox"` to your `Cartfile`.

### To update to a new version:

- Update the gems and pods:
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
- Create a new tag that matches the Mapbox version in `Podfile.lock`
- Create a GitHub release for the tag and upload `Mapbox.framework.zip` as an attachment
