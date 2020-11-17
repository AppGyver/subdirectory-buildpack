# Subdirectory Buildpack

This Heroku buildpack attempts to find the app from a subdirectory and moves its contents to the root level (removing other non-hidden files from the root).

The algorithm attempts to find a `package.json` file in either 1 or 2 levels deep subdirectory. This contents of this folder are moved to the top level.

Do not use this buildpack if do not want to extract a subdirectory, or if you have more than one directory to macth the criteria mentioned above.

To add to your app:

```
heroku buildpacks:add -a <appname> --index=1 https://github.com/AppGyver/subdirectory-buildpack.git
```
