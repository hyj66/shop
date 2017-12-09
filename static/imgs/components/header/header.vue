<template>
    <div class="header">

        <!-- 背景图 -->
        <div class="bg">
            <img :src="seller.avatar" alt="">
        </div>

        <!-- 顶部的上面部分 -->
        <div>
             <!-- 商店主要图片左边 -->
             <div class="tmain" @click='showDetail'>
                  <img :src="seller.avatar" alt="" class="tmain-pic">
             </div>
              <!-- 商店主要图片左边END -->
           

            <!-- 右侧的商家信息 -->
            <div class="tright">
                <div>
                    <!-- 品牌图片 -->
                    <img src="/static/imgs/brand.png" alt="" class="tbrand">
                    <!-- 商店名称 -->
                    <span class="shopname">{{seller.name}}</span>
                </div>
                
                <div>
                    <!-- 快递 -->
                    <span class="shopserver">{{seller.description}}</span>
                </div>
                
                
                <br>
                    <!-- 减图片 -->
                <img src="/static/imgs/decrease.png" alt="" class="decrease">
                     <!-- 在线优惠活动 -->
                <span class="price-lower" v-if='seller.supports'>{{seller.supports[0].description}}</span>
                
            </div> 
            <!-- 右侧的商家信息END -->   

            <!-- 小圆圈 -->
            <div class="circle">
                <p>5个</p>  
                <img src="/static/imgs/big.png" alt="">              
            </div>
            <!-- 小圆圈 END-->

        </div>
        <!-- 顶部的下面部分 -->
        <div class="bt">
            <img src="/static/imgs/bulletin.png" alt="" class="oneimg">
            <div class="details" v-if='seller.supports'>{{seller.bulletin}}</div>
            <span><img src="/static/imgs/big.png" alt=""></span>
        </div>
        <sellerDetail></sellerDetail>
       
    </div>
</template>
<script>
    import {mapGetters,mapState} from 'vuex'
    import sellerDetail from '../sellerDetail/sellerDetail.vue'

    export default {
        // computed:{
        //     ...mapGetters([
        //         'seller'
        //     ])
        // },
         computed:mapState({
             seller:state=>state.seller  //理解为传入state对象，修改state.count属性
          }),
        components:{
            sellerDetail
        },
        methods:{
            showDetail(){
				this.$store.dispatch('showDetail');
			}
        }
    }
</script>
<style lang="less" scoped>
    .header{
        overflow: hidden;
        width:100%;
        height: 2.68rem;
        position:relative;
        background:rgba(7,17,27,0.5);   
        .bg{
            position:absolute;
            left:0;
            right:0;
            top:0;
            bottom:0;
            z-index:-5;
            filter:blur(0.1rem);
            img{
                width:100%;
                height:100%;
            }      
        }
        .tmain{
            display:inline-block;
             .tmain-pic{
                width:1.28rem;
                height:1.28rem;
                margin-top:0.48rem;
                margin-left:0.48rem;
                border-radius: 0.04rem;
            }
        }       
        .tright{
            // border:0.01rem solid red;
            display:flex;
            height:1.28rem;
            margin-left:0.3rem;
            display:inline-block;
            vertical-align: top;
            margin-top:0.48rem;
            .tbrand{
                width:0.60rem;
                height:0.34rem;
                margin-bottom:0.16rem;
               
            }
            .shopname{
                vertical-align: top;
                font-size: 0.32rem;
                color:rgb(255,255,255);
            }
            .shopserver{              
                font-size: 0.24rem;
                color:rgb(255,255,255);
                line-height: 0.24rem;
                
            }
            .price-lower{
                font-size: 0.20rem;
                color:rgb(255,255,255);
                line-height: 0.35rem;
                font-weight: 200;
                vertical-align: top;
                
            }
            .decrease{
                width:0.34rem;
                height:0.34rem;
            }
        }
        .circle{
            // border:0.01rem solid red;
            margin-left:0.54rem;
            margin-top:1rem;
            background:rgba(7,17,27,0.2);
            vertical-align: top;
            height:0.48rem;
            width:0.8rem;
            // horizontal:0.15rem;
            border-radius:0.28rem;
            display:inline-block;
            p{
                margin-top:0.15rem;
                margin-left:0.15rem;
                // border:0.01rem solid red;
                font-size: 0.24rem;
                font-weight: 200;
                line-height: 0.24rem;
                color:rgb(255,255,255);
            }
            img{
                // border:0.01rem solid red;
                display:inline-block;
                vertical-align: top;
                margin-left:0.6rem;
                margin-top:-0.25rem;
                width:0.2rem;
                height:0.2rem;
            }
        }
        .bt{
            line-height: 0.56rem;
            vertical-align: middle;
            height:0.56rem;
            margin-top:0.36rem;
            background:rgba(7,17,27,0.2);
            // border:0.01rem solid red;
            .oneimg{
                margin-top: 0.1rem;
                margin-left: 0.24rem;
                width:0.55rem;
                height:0.32rem;

            }
            .details{
                // border:0.01rem solid red;
                display:inline-block;
                vertical-align: top;
                text-overflow: ellipsis;
                white-space: nowrap;
                overflow: hidden;
                width:6rem;
                margin-left:0.08rem;
                margin-left:0.24rem;
                font-size: 0.20rem;
                color:rgb(255,255,255);
                font-weight: 200;
                line-height:0.56rem;
            }
            span{
                color:white;
                font-size: 0.24rem;
                font-weight: 200;
                vertical-align: top;
                margin-left:0.1rem;
                img{
                    display:inline-block;
                    vertical-align: top;
                    width:0.2rem;
                    height:0.2rem;
                    margin-top:0.2rem;
                }
            }
        }
    }
    
</style>
