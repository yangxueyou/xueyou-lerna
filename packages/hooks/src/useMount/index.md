---
title: useMount
group:
  title: 生命周期
  path: /liftCycle
nav:
  title: hooks
  path: /hooks
  order: 3
---

# useMount

生命周期初始化钩子函数

## 代码演示

```tsx
import React, { useState } from 'react';
import { useMount } from '@xueyou/hooks';
import { Button, Space } from '@xueyou/components';

export default () => {
  const [num, updateNum] = useState(0);

  useMount(() => {
    console.log('我只会在初始化执行');
  });

  return (
    <Space>
      <Button>当前：{num}</Button>
      <Button type="primary" onClick={() => updateNum(num + 1)}>
        +
      </Button>
    </Space>
  );
};
```

## Params

| 参数 | 说明                 | 类型       | 默认值 |
| ---- | -------------------- | ---------- | ------ |
| fn   | 需要被执行的回调函数 | () => void | -      |
