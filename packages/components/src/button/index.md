---
title: Button 按钮
group:
  title: 基础组件
  path: /basis
nav:
  title: 组件库
  path: /components
---

# Button

按钮组件

## 代码演示

```tsx
import React from 'react';
import { Button } from '@xueyou/components';

export default () => {
  const setStyle = () => {
    console.log('111');
  };
  return (
    <>
      <Button
        onClick={() => {
          setStyle();
        }}
      >
        默认按钮
      </Button>
      <br />
      <br />
      <Button type="primary">高亮按钮</Button>
      <br />
      <br />
      <Button type="primary" disabled>
        我被禁用
      </Button>
    </>
  );
};
```

## API

| 属性     | 说明             | 类型                   | 默认值    |
| -------- | ---------------- | ---------------------- | --------- |
| type     | 设置按钮类型     | `primary` \| `default` | `default` |
| onClick  | 点击按钮时的回调 | (event) => void        | -         |
| disabled | 设置按钮禁用     | boolean                | false     |
