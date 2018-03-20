# ScrollAnimation

元素出现在视口添加类（css3动画）（后期可扩展图片懒加载、和无限加载）

>Tips

 观测元素必须包含css样式 visibility: hidden;

## 配置项

| 参数名 | 描述 | 类型 | 默认值 |
| - | :-: | :-: | :-: | 
| el | 被观测的Dom元素(class类名)| String | none |
| option | 包含下面所有参数 | Object |    |
| className | 被观测的元素出现在视口添加动画类名 | String | none  |
|  ratio | 元素可见的比例 | Number | 0.25  |
|  perspective | 开启3d动画模式 | Boolean | false  |
|  parentClassName| 3d动画模式下元素的根元素 | String | none |
|  maxDuration | 动画持续最长时间 | Number|  0.8  |
|  minDuration | 动画持续最短时间  | Number| 0.4 |

### 使用方法
``` bash
  let scrollAnimation = new ScrollAnimation(el,option)
  
  异步更新观测元素
  
  scrollAnimation._refresh()
  
  移除所添加动画类名
  
  scrollAnimation._removeClassAnimation()
  
  当 IntersectionObserver API浏览器不兼容的时候将默认采取添加scroll事件方法处理元素监测，
  此时暴露出移除scroll事件方法
  
  scrollAnimation._destroy()
```
