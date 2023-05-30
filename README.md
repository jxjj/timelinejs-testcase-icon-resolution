# Test Case for TimelineJS3 + Vite Icon resolution error

## Steps to reproduce

1. Clone this repo
2. install dependencies: `npm install`
3. build for production: `npm run build`

## Expected behavior

the build should succeed without warnings about resolving icons.

## Actual behavior

the build produces errors referencing icons in `../../css/icons`.

```console
> timelinejs-test-with-vite4@0.0.0 build
> vite build

vite v4.3.9 building for production...
transforming (53) node_modules/@knight-lab/timelinejs/src/js/media/Media.js
../../css/icons/tl-icons.eot referenced in node_modules/@knight-lab/timelinejs/src/less/TL.Timeline.less didn't resolve at build time, it will remain unchanged to be resolved at runtime

../../css/icons/tl-icons.eot?#iefix referenced in node_modules/@knight-lab/timelinejs/src/less/TL.Timeline.less didn't resolve at build time, it will remain unchanged to be resolved at runtime

../../css/icons/tl-icons.ttf referenced in node_modules/@knight-lab/timelinejs/src/less/TL.Timeline.less didn't resolve at build time, it will remain unchanged to be resolved at runtime

../../css/icons/tl-icons.woff2 referenced in node_modules/@knight-lab/timelinejs/src/less/TL.Timeline.less didn't resolve at build time, it will remain unchanged to be resolved at runtime

../../css/icons/tl-icons.woff referenced in node_modules/@knight-lab/timelinejs/src/less/TL.Timeline.less didn't resolve at build time, it will remain unchanged to be resolved at runtime

../../css/icons/tl-icons.svg#tl-icons referenced in node_modules/@knight-lab/timelinejs/src/less/TL.Timeline.less didn't resolve at build time, it will remain unchanged to be resolved at runtime
✓ 70 modules transformed.
dist/index.html                   0.39 kB │ gzip:  0.27 kB
dist/assets/index-414e53b2.css   70.09 kB │ gzip:  9.11 kB
dist/assets/index-143c441e.js   216.38 kB │ gzip: 64.75 kB
```

## Environment

- macOS 13.4 (22F66)
- Node v18.15.0
