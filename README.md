### react dom diff原理demo实现
安装依赖+启动demo
```
yarn add / npm  i
yarn start /npm start
```

### 虚拟dom
createElement =>{type,props,children}
### dom diff 差异计算
遵循先序深度优先遍历 

 代码逻辑：
 1. 用js模拟dom
 2. 把虚拟dom转换为真实dom 并插入页面
 3. 若有事件发生需改虚拟dom 比较两个虚拟dom差异，得到差异对象 
 4. 把差异对象 应用到真实dom树上

其实 diff 算法的本质就是 找出两个dom 对象中的不同的地方，生成补丁包，根据补丁包给元素一层层递归打补丁 实现最终的视图更新  
