# taxi_effective_v2

[demo v1](https://ingridkao.github.io/taxi_effective/)

## 開發碰到的問題
在手機上會一直閃退
>最後確定的原因是因為地圖所使用上的點位檔案太過龐大，有兩種解法：
a. 透過後端寫一個api去filter geojson大小，目前僅靜態網頁
b. 將點位上傳到[Mapbox tilesets server](https://studio.mapbox.com/tilesets)
兩者現階段接皆無法解決，因此手機版先不呈現地圖只截GIF圖。



## Basic
Project setup
```
npm install
```

Compiles and hot-reloads for development
```
npm run serve
```

Compiles and minifies for production
1. Edit .env.production
vi .env.production
```
VUE_APP_MAPBOXTOKEN = <your access token here>
VUE_APP_BASE_URL = <"/publicPath">
```
2. Build
```
npm run build
```


## Usage
### 1. Version 1
2022三月要再重新build，但一直沒辦法成功，Error message顯示`unable to resolve dependency tree`，用了半天沒辦法成功，由於code並不複雜決定直接拉乾淨的vue3重構。

v1 dependency:
```
"@mapbox/mapbox-gl-sync-move": "^0.3.0",
"@turf/turf": "^6.5.0",
"axios": "^0.21.4",
"core-js": "^3.6.5",
"highcharts": "^9.2.2",
"highcharts-vue": "^1.4.0",
"intersection-observer": "^0.12.0",
"mapbox-gl": "^2.4.1",
"mapbox-gl-compare": "^0.4.0",
"mobile-detect": "^1.4.5",
"scrollama": "^2.2.3",
"video.js": "^7.17.0",
"vue": "^3.0.0"
```
