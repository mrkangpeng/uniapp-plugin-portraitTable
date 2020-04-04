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

<style>

</style>
