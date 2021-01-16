<template>
	<view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad(e) {
			console.log('option',e);
			// redirect to target 
			// if(e && e.url){
			// 	this.redirect(e.url);
			// }
		},
		methods: {
			redirect(link){
				
				let target;
				if(target && target.miniapp){
					wx.navigateToMiniProgram({
					  appId: target.miniapp.appid,
					  path: target.miniapp.path
					})
				}else{
					uni.navigateTo({
						url: target.url
					})
					// window.location.href = this.couponList[i].url
				}
				
			}
		}
	}
</script>

<style>

</style>
