# buildpack-sentry-sourcemaps

This is a simple [Heroku buildpack][] used to uploads JavaScript sourcemaps
to [Bugsnag][], as described in [the Bugsnag docs][docs].

## Usage

Several environment variables are needed:

- `SOURCEMAP_DIR`: the folder (relative to the app root) where the sourcemaps can be found.
- `SOURCEMAP_BUGSNAG_TOKEN`: an authentication token for the Bugsnag API.
- `SOURCEMAP_URL_PREFIX`: the prefix to prepend to each sourcemap. (e.g. `https://example.com/dist/js/`)

Then add this buildpack to your app:

    heroku buildpacks:add https://github.com/ajb/buildpack-bugsnag-sourcemaps

And push a new release.

## License

MIT.

[Heroku buildpack]: https://devcenter.heroku.com/articles/buildpacks
[Bugsnag]: https://www.bugsnag.com/
[docs]: https://docs.bugsnag.com/platforms/browsers/source-maps/
[API page]: https://sentry.io/api/
