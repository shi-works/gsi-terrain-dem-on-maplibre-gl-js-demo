# gsi-terrain-dem-on-maplibre-gl-js-demo
## Public Website
https://shi-works.github.io/gsi-terrain-dem-on-maplibre-gl-js-demo/

## 標高タイルをTerrainRGBに変換するモジュールの使い方
index.htmlのheadに変換モジュールの読み込みを記述
```
<html>

<head>
    <title>国土地理院 標高タイル（DEM10B）</title>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src='./lib/maplibre-gl@2.4.0/maplibre-gl.js'></script>
    <link href='./lib/maplibre-gl@2.4.0/maplibre-gl.css' rel='stylesheet' />
    <script src='./lib/pmtiles@2.10.0/index.js'></script>
    <script type="module" src="maplibre-gl-gsi-terrain-fast-png.js"></script>
```
