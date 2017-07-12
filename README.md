# rollbar-ignore-crawler-errors
Fingerprinting configuration to filter out and ignore errors from common crawlers and bots in [Rollbar](https://rollbar.com/).

## How it works
Groups error messages based on a custom fingerprinting configuration. These errors can then be muted and thus ignored.

## Usage
1. Paste the contents of [fingerprint-config.json](fingerprint-config.json) into the Custom Fingerprinting settings area in Rollbar (Settings > Custom Fingerprinting).
1. Once your first bot hits the site, a new error item called `Crawler JS error` will appear in the main dashboard/items screen. Mute this item and further crawler errors will fall into this muted item, effectively removing them from polluting your true Rollbar items.

## Further reading
See the official Rollbar docs on [filtering and ignoring errors from bots](https://rollbar.com/docs/filter-or-ignore-errors-from-bots/) for further integration details.
