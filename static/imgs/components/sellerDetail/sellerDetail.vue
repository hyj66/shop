<template>
	<transition enter-active-class = 'animated tada' leave-active-class = 'animated tada'>
		<div>
			<div class="sellerDetail" v-show='sellerShow'>
				<!-- 整个页面 -->
				<div class="hides" @click='hideDetail'>
					<!-- 第一部分 -->
					<div class="tops">
						<div class="contentone">
							<!-- 文字 -->
							<p>{{seller.name}}</p>
							<!-- 星星 -->
							<div class="star">五角星</div>
						</div>
						<!-- 横县中间夹着文字部分 -->
						<div class="hrs">
							<hr>
							<p>优惠信息</p>
							<hr>
						</div>
					</div>
					
					<!-- 第二部分 -->
					<div class="mids">
						<div class="content">
							<div class="content-item">
								<img src="/static/imgs/decrease.png" alt="">
								<p>我们的优惠信息是什么呢我们的</p>
							</div>
							<div class="content-item">
								<img src="/static/imgs/discount.png" alt="">
								<p>我们的优惠信息是什么呢我们的</p>
							</div>
							<div class="content-item">
								<img src="/static/imgs/discount.png" alt="">
								<p>我们的优惠信息是什么呢我们的</p>
							</div>
							<div class="content-item">
								<img src="/static/imgs/special.png" alt="">
								<p>我们的优惠信息是什么呢我们的</p>
							</div>
							<div class="content-item">
								<img src="/static/imgs/special.png" alt="">
								<p>我们的优惠信息是什么呢我们的</p>
							</div>
						</div>
						
					</div>
					<!-- 第三部分 -->
					<div class="bots">
						<div class="hrs">
							<hr>
							<p>商家公告</p>
							<hr>
						</div>
						<div class="texts">里面是文字里面是文字
							里面是文字里面是文字里面是文字里面是文字</div>
					</div>
					<!-- 第四部分 -->
					<div class="closed">
						<img src="/static/imgs/close.png" alt="">
					</div>
				</div>				
			</div>
		</div>
		
		
	</transition>
</template>

<script>
	import { mapState,mapGetters } from 'vuex'
	import animate from 'animate.css'

	export default{
		computed: mapGetters([
		  // 映射 this.count 为 store.state.count
		  'seller',
		  'sellerShow'
		]),
		methods:{
			hideDetail(){
				this.$store.dispatch('hideDetail');
			}
		}

	}
</script>

<style lang='less' scoped>
	.sellerDetail{
		padding-bottom:1rem;;
		height:100%;
		width: 100%;
		height: 100%;
		position: fixed;
		left: 0;
		top: 0;
		background: #ddd;
		.hides{
			width: 100%;
			height: 100%;
			border: 1px solid #000;
			background-color:rgba(7,17,27,0.8);
			// filter:blur(0.1rem);
			.tops{
				box-sizing: border-box;
				// border:0.2px solid black;
				width:100%;
				height: 4rem;
				.contentone{
					// border: 2px solid yellow;
					width:4.8rem;
					height:1.62rem;
					margin:0.58rem auto;
					p{
						margin:0 auto;
						text-align: center;
						// border: 1px solid green;
						width:3.8rem;
						height:0.62rem;
						font-size: 0.32rem;
						color:rgb(255,255,255);
						font-weight: 700;
						line-height: 0.32rem;
						margin-top:0.128rem;
						}
						
						.star{
							margin-top:0.22rem;
							text-align: center;
							// border: 1px solid green;
							width:4.8rem;
							height:0.62rem;
						}
				}
				.hrs{
						margin:0 auto;
						margin-top:-0.4rem;
						width:6.1rem;
						height: 0.2rem;
						// border: 2px solid green;
						p{
							margin:0 auto;
							margin-top:0rem;
							width:1.3rem;
							vertical-align: center;
							text-align: center;
							color:white;
							font-size:0.28rem;
							font-weight: 700;
							background-color:rgba(7,17,27,0.1); 
							display:inline-block;
						}
						hr{
							color:rgb(255,255,255,0.2);
							display:inline-block;
							width:2.24rem;
						}
					}
				
			}
			.mids{
				box-sizing: border-box;
				// border:1px solid red;
				margin-top:-1.4rem;
				width:100%;
				height: 5rem;
				
				.content{
					vertical-align: center;
					// border:1px solid green;
					margin:0 auto;
					width:6rem;
					height:4.6rem;
				
					.content-item{
						// border:1px solid red;
						margin-top:0.2rem;
						width:6rem;
						height:0.7rem;
						vertical-align: center;
						text-overflow: ellipsis;
						white-space: nowrap;
						overflow: hidden;
						p{
							display: inline-block;
							vertical-align: top;
							font-size: 0.24rem;
							font-weight: 200;
							color:rgb(255,255,255);
							line-height: 0.7rem;
							width:5rem;
							text-overflow: ellipsis;
							white-space: nowrap;
							overflow: hidden;
						}
					}
				}
			}
			.bots{
				box-sizing: border-box;
				// border:1px solid red;
				width:100%;
				height: 4rem;
				.hrs{
						margin:0 auto;
						margin-top:0.12rem;
						width:6.1rem;
						height: 0.2rem;
						// border: 2px solid green;
							p{
								margin:0 auto;
								width:1.3rem;
								vertical-align: center;
								text-align: center;
								color:white;
								font-size:0.28rem;
								font-weight: 700;
								background-color:rgba(7,17,27,0.1); 
								display:inline-block;
								}
							hr{
								color:rgb(255,255,255,0.2);
								display:inline-block;
								width:2.24rem;
							}
					}
					.texts{
						border: 2px solid green;
						width:5.32rem;
						height:2.8rem;
						margin:0 auto;
						margin-top:0.3rem;
						text-overflow: ellipsis;
						// white-space: nowrap;
						overflow: hidden;
						font-size:0.24rem;
						font-weight: 200;
						color:rgb(255,255,255);
						lighting-color: 0.48rem;
					}
			}
			.closed{
				width:100%;
				height: 1rem;
				// border:1px solid red;
				// 百度的方法把X放在地步固定住
				height:1rem;
				margin:-1rem auto 0 auto;
				position: relative;
				clear:both;
				font-size: 0.64rem;
				text-align: center;
				img{
					margin:0 auto;
					margin-top:0.01rem;
					width:0.64rem;
					height:0.64rem;
				}
			}
		}
	}
</style>