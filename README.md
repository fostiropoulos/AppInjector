# AppInjector

Inject code into Android Application files to restrict and monitor API access on the mobile device.
Enhance security and privacy of the mobile device. Effectively deny permissions to the application by
replacing its permission­sensitive API calls with calls to injected functions that return fake data,
protecting the user’s identity and restricting other sensitive features. Use these injected functions to also
monitor and log the application’s use of sensitive API calls.

## Motivation
Many Android apps require a long list of approved permissions before the user may install them, but
stock Android does not offer mechanisms for the user to block these permissions or to see how they
are used. In some older versions of Android, there was a hidden App Ops feature, but using this to
block permissions would make many apps that depend on these permissions crash because of uncaught
exceptions thrown by API calls when the permission is not available. Our solution should allow apps
with blocked permissions to continue operating successfully with our fake data instead of crashing.
