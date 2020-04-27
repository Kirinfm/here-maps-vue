# here-maps-vue
Vue components library for HERE Maps

[here map](https://developer.here.com/)

* install here-maps-vue
```
// 若需要加载自己的ui样式, 修改 ui-theme/mapjs-ui.css, 再进行导入覆盖
import './assets/map-ui-theme/index.css'
import HereMap from '@/components/HereMap'
Vue.use(HereMap, {
  // v3.1版本移除了 appcode 和 appid, 以 apiKey 作为替代方案
  apiKey: 'yourApiKey',
  customUICss: true
})
```
* add here-map componet
```
<h-map
    :center="{ lat: 0, lng: 0 }"
    :zoom="12.5"
    :style="{ height: '500px' }"
    :map-style="mapStyle"
    layer-language="zh"
    :mapsettings-ui="false"
    @ready="mapReady"
  />
```
* add marker and domMarker component
```
<h-dom-marker
      :position="{ lng: 0, lat: 0}"
      :draggable="true"
      :volatility="true"
      :icon="{url: icon, size:{width:20,height:20}}"
      :rotation="180"
    >
</h-dom-marker>
<h-marker
      :position="{ lng: 0, lat: 0}"
      :icon="{url: icon, size:{width:20,height:20}}"
    >
</h-marker>
```
* add InfoBubble component
```
<h-info-bubble ref="bubble" :position="{ lng: 0, lat: 0 }">
    <template><span>hello</span></template>
</h-info-bubble>
```