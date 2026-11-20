# 颜真卿 · 祭侄文稿

颜真卿《祭侄文稿》（台北故宫博物院藏） — a narrated deep-zoom reading, as a static page (in Chinese).

Yan Zhenqing's Draft of a Requiem to My Nephew (National Palace Museum, Taipei), the whole handscroll: the draft's 24 columns read one by one — struck-out characters grey, additions red — and its colophons.

Live: https://youdata.github.io/jizhi-gao/

The image pyramid is a tile folder (`jizhi/`: `header.idx` + `{z}/{x}/{y}.png`), so any static host serves it.
Its fonts are in `fonts/`, trimmed to the page's characters. The narrated video is not included.

## How it is made

From `infographic-examples/jizhi-gao/build.mjs` (the page) with rx (`~/rx-cli`):

```sh
node build.mjs                                                     # → jizhi-gao.json
rx export jizhi-gao.json --out site --app /rx-graphic-editor/web/index.html --canvas --theme dark --lock-layers --tiles dir
rx publish site --to github:youdata/jizhi-gao --yes
```
