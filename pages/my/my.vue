<template>
	<view>
		<!-- 头部 -->
		<view class="position-relative d-flex a-center animated fadeIn faster" style="height: 320rpx;">
			<!-- 消息列表 -->
			<view class="iconfont icon-xiaoxi position-absolute text-white" style="font-size: 50rpx;top: 75rpx;right: 20rpx;z-index: 100;"></view>

			<image src="../../static/images/bg.jpg" style="height: 320rpx;width: 100%;"></image>

			<view class="d-flex a-center position-absolute left-0 right-0" style="bottom: 50rpx;">
				<image src="/static/images/demo/demo6.jpg" style="height: 145rpx;width: 145rpx;border: 5rpx solid;" class="rounded-circle border-light ml-4"></image>
				<view class="ml-2 text-white font-md" @click="totest">登录/注册</view>
				<view
					class="d-flex a-center j-center a-self-end ml-auto px-2"
					style="height: 70rpx;background: #FFD43F;color: #CC4A00;border-top-left-radius: 40rpx;border-bottom-left-radius: 40rpx;"
				>
					<view class="line-h iconfont icon-huangguan mr-1"></view>
					会员积分 0.00
				</view>
			</view>
		</view>

		<card>
			<view slot="title" class="d-flex a-center j-sb w-100">
				<text class="font-md font-weight">我的订单</text>
				<view class="text-secondary font ml-auto">
					全部订单
					<text class="iconfont icon-you font"></text>
				</view>
			</view>
			<view class="d-flex a-center">
				<view class="flex-1 d-flex flex-column a-center j-center py-3" hover-class="bg-light-secondary">
					<view class="iconfont font-lg line-h iconfont icon-fuzhi"></view>
					<view>待付款</view>
				</view>
				
				<view class="flex-1 d-flex flex-column a-center j-center py-3" hover-class="bg-light-secondary">
					<view class="iconfont font-lg line-h iconfont icon-daishouhuo"></view>
					<view>待发货</view>
				</view>
				
				<view class="flex-1 d-flex flex-column a-center j-center py-3" hover-class="bg-light-secondary">
					<view class="iconfont font-lg line-h iconfont icon-gouwuche"></view>
					<view>待收货</view>
				</view>
				
				<view class="flex-1 d-flex flex-column a-center j-center py-3" hover-class="bg-light-secondary">
					<view class="iconfont font-lg line-h iconfont icon-pinglun"></view>
					<view>待评价</view>
				</view>
				
			</view>
		</card>

		<divider></divider>

		<uni-list-item showExtraIcon leftIconStyle="color:#FDBF2E;" leftIcon="icon-VIP" title="小米会员"></uni-list-item>
		<uni-list-item showExtraIcon leftIconStyle="color:#FCBE2D;" leftIcon="icon-huangguan" title="会员中心"></uni-list-item>
		<uni-list-item showExtraIcon leftIconStyle="color:#FA6C5E;" leftIcon="icon-service" title="服务中心"></uni-list-item>
		<uni-list-item showExtraIcon leftIconStyle="color:#FE8B42;" leftIcon="icon-home" title="小米之家"></uni-list-item>
		<uni-list-item showExtraIcon leftIconStyle="color:#9ED45A;" leftIcon="icon-gengduo" title="更多功能"></uni-list-item>
		<divider></divider>
		<uni-list-item showExtraIcon leftIconStyle="color:#808C98;" leftIcon="icon-icon_set_up" title="更多设置"></uni-list-item>
	</view>
</template>

<script>
import card from '@/components/common/card.vue';
export default {
	components: {
		card
	},
	methods:{
		totest(){
			uni.navigateTo({
				url:'/pages/test/test'
			})
		}
	}
};
</script>

<style></style>
