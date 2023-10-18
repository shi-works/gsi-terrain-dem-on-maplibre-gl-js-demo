# gsi-terrain-dem-on-maplibre-gl-js-demo
## Public Website
https://shi-works.github.io/gsi-terrain-dem-on-maplibre-gl-js-demo/

## 標高タイルをTerrainRGBに変換するモジュールの使い方
- index.htmlのheadに変換モジュール(maplibre-gl-gsi-terrain-fast-png.js)の読み込みを記述します。
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
- index.htmlのmap.addSource内のtilesを下記のとおりにします。
- `gsidem://https://cyberjapandata.gsi.go.jp/xyz/dem_png/{z}/{x}/{y}.png`とすることで、標高タイルがTerrainRGBに変換されます。
```
            map.addSource("gsidem", {
                type: 'raster-dem',
                tiles: [
                    'gsidem://https://cyberjapandata.gsi.go.jp/xyz/dem_png/{z}/{x}/{y}.png',
                ],
                attribution: '<a href="https://maps.gsi.go.jp/development/ichiran.html#dem" target="_blank">地理院タイル(標高タイル)</a>',
                tileSize: 256
            });
```
