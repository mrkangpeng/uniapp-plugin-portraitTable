### 简易版纵向表头table

> 参数介绍

* tableData(列表数据，一般是后台返回的数据)
* title(表头数据，自己定义，lable代表表头名称，value对应tableData中的字段名)
* align(数据显示方式 left | center | right)
* titleBg(表头背景颜色)

> 例子

```javascript
<template>
	<view class="content">
		<p-table :tableData="tableData" :title="title" align="center" titleBg="#eee"></p-table>
	</view>
</template>
<script>
import pTable from '@/components/portrait_table/portrait_table.vue'
export default {
	components:{
		pTable
	},
	data() {
		return {
			title: [
				{
					label: '名字',
					value: 'name'
				},
				{
					label: '性别',
					value: 'sex'
				},
				{
					label: '年龄',
					value: 'age'
				},
				{
					label: '爱好',
					value: 'hobby'
				}
			],
			tableData: [
				{
					name:'小明',
					sex:'男',
					age:18,
					hobby:'唱'
				},
				{
					name:'小刚',
					sex:'男',
					age:21,
					hobby:'跳'
				},
				{
					name:'小芳',
					sex:'男',
					age:19,
					hobby:'rap'
				},
				{
					name:'小张',
					sex:'男',
					age:20,
					hobby:'篮球'
				},
			]
		}
	},
	onLoad() {

	},
	methods: {

	}
}
</script>
```
> 写在最后
创作不易，好用请点个赞吧！