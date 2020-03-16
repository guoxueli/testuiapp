<template>
	<view class="content">

		<scroll-view>
			<view class="box" v-for="(item,index) in list" :key="index">{{item.title}}</view>
		</scroll-view>
		<scroll-view>
			<view v-for="(item,index) in list" :key="index">
				<view>{{item.title}}</view>
				<view v-for="(i,v) in item" :key="v">{{i}}</view>
			</view>
		</scroll-view>


	</view>
</template>

<script>
	import test from '../../compents/test.vue'
	export default {
		components: {
			test
		},
		data() {
			return {
				title: 'Hello',
				list: [{
						title: '女装',
						list: ['上衣', '短裤', '牛仔裤', '短袖', '长袖']
					},
					{
						title: '童装',
						list: ['上衣', '短裤', '牛仔裤', '短袖', '长袖']
					},
					{
						title: '男装',
						list: ['上衣', '短裤', '牛仔裤', '短袖', '长袖']
					},
					{
						title: '老年装',
						list: ['上衣', '短裤', '牛仔裤', '短袖', '长袖']
					},
				]
			}
		},
		onLoad() {

		},
		methods: {
			handleClick(rel) {
				console.log(rel)
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
	}
</style>
