<template>
	<view>
		<view class="p-2">
			<view class="d-flex a-center py-2 border-bottom border-light-secondary text-muted">
				<text>用户评价(123)</text>
				<text class="main-text-color ml-auto mr-1">98%</text>
				<text class="text-muted">满意</text>
			</view>
			
			<view class="d-flex flex-wrap pt-2" style="margin-right: -20rpx;">
			  <view class="px-2 py border rounded mr-2 mb-2 cate-item"
				v-for="(item,index) in cateList" :key="index"
			  :class="cateIndex === index ? 'active' : '' "
				@tap="cateChange(index)">
		    	{{item.name}}
		    </view>
			</view>
		</view>
		<divider></divider>
		
		<view class="d-flex p-2 a-start border-bottom border-light-secondary">
			<image src="../../static/images/demo/demo6.jpg" mode="widthFix"
			style="width: 90rpx;height: 90rpx;"
			class="rounded flex-shrink"></image>
			<view class="pl-2 flex-1">
				<!-- header -->
				<view class="d-flex a-center">
					<text class="font-md text-primary font-weight" style="margin-right: auto;">昵称</text>
					<view class="iconfont icon-service" style="color: #DE7232;">
						<text class="pl-1 font">超爱</text>
					</view>
				</view>
				<!-- body -->
				<view class="line-h-md font-md">
					非常好
				</view>
				<view class="row">
					<view class="span24-8 px pb">
						<image src="../../static/images/demo/cate_07.png" mode="widthFix"
						style="height: 100rpx;"></image>
					</view>
				</view>
				<!-- header -->
				<view class="d-flex a-center">
					<text class="text-light-muted" style="margin-right: auto;">2022-08-12</text>
					<view class="d-flex text-light-muted a-center mr-1">
						0<text class="iconfont icon-dianzan text-muted ml-1"></text>
						</view>
					<view class="d-flex text-light-muted a-center mr-1">
						10<text class="iconfont icon-pinglun text-muted ml-1"></text>
					</view>
				</view>
				<!-- 客服回复 -->
		    <view class="bg-light-secondary rounded p-2 d-flex flex-wrap a-center mt-2 ">
					<text class="main-text-color">官方回复：</text>
					哈哈哈哈哈哈
					<view class="iconfont icon-dianzan text-light-muted line-h-md font ml-2">
						<text class="text-muted pl-1">赞客服122</text>
					</view>
				</view>
			</view>
		</view>
		
	</view> 
</template>

<script>

	export default{
		data(){
			return{
				cateIndex:0,
				cateList:[
					{name:"全部"},
					{name:"有图"},
					{name:"非常喜欢"},
					{name:"拍照好"},
					{name:"屏幕nice"},
					{name:"手感很棒"},
					{name:"性能好"},
				]			
		  }	
	  },
		methods:{
			cateChange(index){
				this.cateIndex = index
			}
		}
	}
</script>

<style>
	.cate-item{
	background:#FFEBEC;
	color: #7B6D6C;
	border-color:#F4E0E1;
	}
	.cate-item.active{
	background:#dc3544!important;
	color: #FFFFFF!important;
	border-color: #DE7232!important;
	}

</style>