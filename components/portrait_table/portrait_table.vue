<template>
	<view class="table">
		<view class="thead">
			<view 
				:style="{textAlign:align,backgroundColor:titleBg}"
				class="title" 
				v-for="(item, index) in title" 
				:key="index">
				<text>{{ item.label }}</text>
			</view>
		</view>
		<view class="tbody_wrap">
			<view class="tbody">
				<view class="col" v-for="(item, index) in title" :key="index">
					<view class="row" 
					:style="{textAlign:align}"
					:class="[index == 1 ? 'firstCol' : 'baseBg']"
					 v-for="(zItem, zIndex) in tableData" 
					 :key="zIndex">
						<text>{{ zItem[item.value] || '-' }}</text>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
		};
	},
	props: {
		tableData: {
			type: Object,
			required: true
		},
		title: {
			type: Object,
			required: true
		},
		align:{
			type:String,
			default:'center'
		},
		titleBg:{
			type:String,
			default:'#fff'
		}
	},
	methods: {},
};
</script>

<style lang="less">
.table {
	display: flex;
	.thead {
		border-bottom: 1rpx solid #e5e5e5;
		box-shadow: 5rpx 0 5rpx #eee,;
		.title {
			box-sizing: border-box;
			position: relative;
			padding: 0 20rpx;
			min-width: 180rpx;
			height: 88rpx;
			line-height: 88rpx;
			font-size: 24rpx;
			color: #666;
			border: 1rpx solid #e5e5e5;
			border-bottom: none;
			border-right: none;
		}
	}
	.tbody_wrap {
		overflow-x: auto;
		border-right: 1rpx solid #e5e5e5;
		border-bottom: 1rpx solid #e5e5e5;
		.tbody {
			.col {
				display: flex;
			}
			.row {
				box-sizing: border-box;
				padding: 0 20rpx;
				line-height: 88rpx;
				font-size: 24rpx;
				color: #666;
				min-width: 180rpx;
				height: 88rpx;
				border: 1rpx solid #e5e5e5;
				border-bottom: none;
				border-right: none;
			}
		}
	}
}
.baseBg{
	background-color: #fff;
}
.firstCol{
	background-color: #007AFF;
}
</style>
