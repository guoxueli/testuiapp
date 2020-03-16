<template>
	<view>
		<text>我是test组件{{msg}}</text>
		<button type="primary" @click="test()">点击触发事件</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {}
		},
		props: {
			msg: {
				type: String,
				default: ''
			}
		},
		methods: {
			test() {
				this.$emit('handleClick', {
					str: 'etwet'
				})
			}
		}
	}
</script>

<style>
</style>
