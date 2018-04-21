:::demo `data` 选项传入一个数组，数组里的每一项须包含 `{ name, type }` 字段，组件会根据 `type` 进行分组。通过 `selected.sync` 进行变量绑定。 

```html
<template>
  <bdi-index-filter :data="options" :selected.sync="selected"></bdi-index-filter>
</template>
<script>
export default {
  data () {
    return {
      options: [
        {
          "id": 1,
          "name": "交易额",
          "type": "常规"
        },
        {
          "id": 2,
          "name": "有效订单量",
          "type": "常规"
        },
        {
          "id": 3,
          "name": "实付金额",
          "type": "常规"
        },
        {
          "id": 4,
          "name": "产品收入",
          "type": "常规"
        },
        {
          "id": 5,
          "name": "下单用户数",
          "type": "常规"
        }
      ],
      selected: []
    }
  }
}
</script>
```
:::