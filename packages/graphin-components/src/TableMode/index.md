# TableMode

TableMode 表格模式是一种系统组件，虽然不能直观展示图中关联关系，但是对于罗列点、边属性信息有较大优势，作为分析能力的一个补充。

## 功能特性

- TableMode 数据源应该和 Graphin.props.data 保持一致，用表格渲染

## 参考资料

> 欢迎 github 的伙伴 讨论设计和组件方案，开源共建。

- ![](https://gw.alipayobjects.com/mdn/rms_402c1a/afts/img/A*iNtkTIpsuKYAAAAAAAAAAAAAARQnAQ)

## 用法

```tsx
import React from 'react';
import ReactDOM from 'react-dom';
import Graphin, { Utils } from '@antv/graphin';
import { TableMode } from '@antv/graphin-components';
// Do not forget to import CSS
import '@antv/graphin/dist/index.css';
import '@antv/graphin-components/dist/index.css';

const data = Utils.mock(10).graphin();
const App = () => {
  return (
    <div className="App">
      <Graphin data={data}>
        <TableMode data={data} />
      </Graphin>
    </div>
  );
};

const rootElement = document.getElementById('root');
ReactDOM.render(<App />, rootElement);
```