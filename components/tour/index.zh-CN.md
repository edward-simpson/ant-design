---
category: Components
subtitle: 漫游式引导
group: 数据展示
title: Tour
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*8CC_Tbe3_e4AAAAAAAAAAAAADrJ8AQ/original
coverDark: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*nF6hQpM0XtEAAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
---

用于分步引导用户了解产品功能的气泡组件。自 `5.0.0` 版本开始提供该组件。

## 何时使用

常用于引导用户了解产品功能。

## 代码演示

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">基本</code>
<code src="./demo/non-modal.tsx">非模态</code>
<code src="./demo/placement.tsx">位置</code>
<code src="./demo/mask.tsx">自定义遮罩样式</code>
<code src="./demo/indicator.tsx">自定义指示器</code>
<code src="./demo/render-panel.tsx" debug>\_InternalPanelDoNotUseOrYouWillBeFired</code>

## API

### Tour

| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| arrow | 是否显示箭头，包含是否指向元素中心的配置 | `boolean` \| `{ pointAtCenter: boolean}` | `true` |  |
| placement | 引导卡片相对于目标元素的位置 | `left` `leftTop` `leftBottom` `right` `rightTop` `rightBottom` `top` `topLeft` `topRight` `bottom` `bottomLeft` `bottomRight` | `bottom` |  |
| onClose | 关闭引导时的回调函数 | `Function` | - |  |
| onFinish | 引导完成时的回调 | `Function` | - |  |
| mask | 是否启用蒙层，也可传入配置改变蒙层样式和填充色 | `boolean \| { style?: React.CSSProperties; color?: string; }` | `true` |  |
| type | 类型，影响底色与文字颜色 | `default` \| `primary` | `default` |  |
| open | 打开引导 | `boolean` | - |  |
| onChange | 步骤改变时的回调，current 为当前前的步骤 | `(current: number) => void` | - |  |
| current | 当前处于哪一步 | `number` | - |  |
| scrollIntoViewOptions | 是否支持当前元素滚动到视窗内，也可传入配置指定滚动视窗的相关参数 | `boolean \| ScrollIntoViewOptions` | `true` | 5.2.0 |
| indicatorsRender | 自定义指示器 | `(current: number, total: number) => ReactNode` | - | 5.2.0 |
| zIndex | Tour 的层级 | number | 1001 | 5.3.0 |

### TourStep 引导步骤卡片

| 属性 | 说明 | 类型 | 默认值 | 版本 |
| --- | --- | --- | --- | --- |
| target | 获取引导卡片指向的元素，为空时居中于屏幕 | `() => HTMLElement` \| `HTMLElement` | - |  |
| arrow | 是否显示箭头，包含是否指向元素中心的配置 | `boolean` \| `{ pointAtCenter: boolean}` | `true` |  |
| cover | 展示的图片或者视频 | `ReactNode` | - |  |
| title | 标题 | `ReactNode` | - |  |
| description | 主要描述部分 | `ReactNode` | - |  |
| placement | 引导卡片相对于目标元素的位置 | `left` `leftTop` `leftBottom` `right` `rightTop` `rightBottom` `top` `topLeft` `topRight` `bottom` `bottomLeft` `bottomRight` `bottom` |  |  |
| onClose | 关闭引导时的回调函数 | `Function` | - |  |
| mask | 是否启用蒙层，也可传入配置改变蒙层样式和填充色，默认跟随 Tour 的 `mask` 属性 | `boolean \| { style?: React.CSSProperties; color?: string; }` | `true` |  |
| type | 类型，影响底色与文字颜色 | `default` \| `primary` | `default` |  |
| nextButtonProps | 下一步按钮的属性 | `{ children: ReactNode; onClick: Function }` | - |  |
| prevButtonProps | 上一步按钮的属性 | `{ children: ReactNode; onClick: Function }` | - |  |
| scrollIntoViewOptions | 是否支持当前元素滚动到视窗内，也可传入配置指定滚动视窗的相关参数，默认跟随 Tour 的 `scrollIntoViewOptions` 属性 | `boolean \| ScrollIntoViewOptions` | `true` | 5.2.0 |
