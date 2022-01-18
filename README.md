## 1.安装：

```powershell
npm install vue-particles--save-dev
```

## 2. 在main.js中引入

```jsx
import VueParticles from 'vue-particles'
Vue.use(VueParticles)
```

## 3.使用

```jsx
  <div id="app">
    <vue-particles
      color="#646775"
      :particleOpacity="0.7"
      :particlesNumber="90"
      shapeType="circle"
      :particleSize="2"
      linesColor="#2E3143"
      :linesWidth="2"
      :lineLinked="true"
      :lineOpacity="0.9"
      :linesDistance="148"
      :moveSpeed="2"
      :hoverEffect="true"
      hoverMode="grab"
      :clickEffect="true"
      clickMode="push"
      class="lizi"
    ></vue-particles>
    <router-view />
  </div>
```

## 4.样式：

```css
.lizi {
  background-color: #080c22;
}
```

## 5.遇到的坑

我是在想在整个vue项目中，将动态粒子作为背景图来用，当有新的div需要呈现时，会发现div是不能覆盖`vue-particles` 内容的，会依次靠后显示，解决方法：

将`vue-particles`的默认样式`#particles-js` 设置`position: absolute`; 新的div 样式设置 `position: relative`;