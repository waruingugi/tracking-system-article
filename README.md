# The Hidden Problem

How we built a system that tracks thousands of vehicles live: one log, three readers, alerts that fire once, and webhooks that never slow search. An engineering story with interactive maps.

Read it here: https://waruingugi.github.io/tracking-system-article/

## What the article covers

- Why "where is every vehicle right now?" gets hard when thousands of phones ask it every minute.
- The one rule: every position goes into one log first, and three readers each build their own view from it.
- Logging phones in once, then letting their pings flow freely.
- Finding the nearest vehicle fast, first in a straight line, then by road.
- Alerts that fire once, and webhooks where one slow customer never slows anyone else.
- Replaying a trip to settle an argument.
- What it costs to run, with a calculator you can try for your own fleet.

## What's in this repo

- `index.html` is the whole article.
- `figs/` holds the interactive figures. The article loads each one in a frame.

There is no build step and nothing to install. It's plain HTML, CSS and JavaScript.

## Reading it on your own computer

Open `index.html` in a browser. If a figure stays blank, serve the folder instead:

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Notes

- Every number about fleet size, cost and storage is a rounded, rough estimate. None of them comes from a real customer.
- The maps show Cape Town. Map data © OpenStreetMap contributors, available under the Open Database License.
- Fonts come from Google Fonts.
