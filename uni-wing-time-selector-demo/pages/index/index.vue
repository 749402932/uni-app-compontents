<template>
	<view class="content">
		<TimeSelector @btnConfirm="btnConfirm" @btnCancel="btnCancel">
			<view class="box-title">{{ title }}</view>
			<view class="box-time">{{ time }}</view>
		</TimeSelector>
	</view>
</template>

<script>
import TimeSelector from '@/comontents/wing-time-selector/wing-time-selector.vue';
export default {
	components: {
		TimeSelector
	},
	data() {
		return {
			title: '当前选择器',
			time: new Date()
		};
	},
	onLoad() {},
	methods: {
		btnConfirm(e) {
			console.log('确定时间为：', e);
			this.time = e.value;
			this.title = '当前选择时间';
		},
		btnCancel() {
			console.log('取消时间：', e);
		}
	}
};
</script>

<style>
.box-title {
	margin: 24rpx;
	font-size: 40rpx;
	font-weight: bold;
	color: #333333;
}
.box-time {
	margin: 24rpx;
	font-size: 30rpx;
	color: #3496fb;
}
</style>
