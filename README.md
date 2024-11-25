# Background
This repository showcases methods to open an app's settings page on iOS. This is useful for guiding users to configure permissions or settings


# Methods Overview
## prefs:root
An older URL scheme to access specific system settings:
```
let url = URL(string: "prefs:root=General")!
UIApplication.shared.open(url)
```

## prefs:
A simplified scheme to open general settings:

```
let url = URL(string: "prefs:")!
UIApplication.shared.open(url)
```

## app-prefs:
A more modern scheme for app-specific settings:
```
let url = URL(string: "app-prefs:root=APP_BUNDLE_ID")!
UIApplication.shared.open(url)
```

## settings-navigation:
If none of the above works, try the following:
```
let url = URL(string: "settings-navigation://com.apple.Settings.Apps/APP_BUNDLE_ID")!
UIApplication.shared.open(url)


```
