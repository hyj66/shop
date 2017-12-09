<template>
    <div class="ratings">
       <!-- 上部分 -->
       <div class="tops">
           <div class="left">
              <div class="score">3.9</div>
              <div class="zong">综合评分</div>
              <div class="compare">高于周边商家69.2%</div>
           </div>
           <div class="right">
               <div class="content">
                    <div class="rig one">
                        <span>服务态度</span>
                        <div class="star">
                            <img src="/static/imgs/star_on.png" alt="">
                            <img src="/static/imgs/star_on.png" alt="">
                            <img src="/static/imgs/star_on.png" alt="">
                            <img src="/static/imgs/star_off.png" alt="">
                            <img src="/static/imgs/star_off.png" alt="">
                        </div>
                        <div class="score">3.9</div>
                    </div>
                    <div class="rig two">
                        <span>服务态度</span>
                        <div class="star">
                            <img src="/static/imgs/star_on.png" alt="">
                            <img src="/static/imgs/star_on.png" alt="">
                            <img src="/static/imgs/star_on.png" alt="">
                            <img src="/static/imgs/star_off.png" alt="">
                            <img src="/static/imgs/star_off.png" alt="">
                        </div>
                        <div class="score">4.0</div>
                    </div>
                    <div class="rig three">
                        <span>送达时间</span>
                        <div class="times">
                           44分钟
                        </div>
                    </div>
               </div>
               
           </div>
       </div>
       <!-- 上部分 endddd++++++++-->

       <!-- 空白部分 ++++++++-->
       <div class="whites"></div>
       <!-- 空白分 enddd++++-->
       <!-- 下中部分++++++ -->
       <div class="mids">
           <div class="one">
               <div class="all">
                   <span class="one">全部</span>
                   
              </div>
               <div class="fellgood">
                   <span class="one">满意</span>
                   <!-- <span class="two">57</span> -->
                </div>
                <div class="fellbad">
                   <span class="one">不满意</span>
                   <!-- <span class="two">57</span> -->
                </div>
           </div>
           <div class="two">
               <div class="trues">
                   <img src="/static/imgs/true.png" alt="">
               </div>
               <div class="secontent">只看有内容的评价</div>
           </div>
       </div>
       <!-- 下中部分 +++++++enddd-->

       <!-- 底部 ++++++-->
       <div class="bt">
           <div class="rurn">
               <div class="one">
                   <div class="peoplepic">
                        <img src="/static/imgs/special.png" alt="">
                    </div>
               </div>
               <div class="two">000</div>
               <div class="three">0000</div>
           </div>
       </div>
       <!-- 底部enddd ++++++-->
    </div>
</template>
<script>
    export default{

    }
</script>
<style lang='less' scoped>
    .ratings{
        width:100%;
        height:100%;
        .tops{
            // border:1px solid red;
            border-bottom:1px solid rgba(7,17,27,0.1);
            box-sizing: border-box;
            width:100%;
            height: 2.1rem;
            display:flex;
            .left{
                // border:1px solid red;
                box-sizing: border-box;
                display:inline-block;
                width:2.75rem;
                height: 2.1rem;
                flex:1;
                .score{
                    // border:1px solid red;
                    width:100%;
                    height:0.56rem;
                    margin-top:0.36rem;
                    text-align: center;
                    font-size: 0.48rem;
                    line-height: 0.56rem;
                    color:rgb(255,153,0);
                }
                .zong{
                    // border:1px solid red;
                    width:100%;
                    height:0.24rem;
                    margin-top:0.12rem;
                    text-align: center;
                    font-size: 0.24rem;
                    line-height: 0.24rem;
                    color:black;
                }
                .compare{
                    // border:1px solid red;
                    width:100%;
                    height:0.2rem;
                    margin-top:0.12rem;
                    text-align: center;
                    font-size: 0.2rem;
                    line-height: 0.2rem;
                    color:rgb(147,153,159);
                }
            }
            .right{
                border-left:1px solid rgba(7,17,27,0.1);
                flex:1.7;
                box-sizing: border-box;
                display:inline-block;
                width:4rem;
                height: 2.1rem;
                .content{
                    // border:1px solid red;
                    margin-left:0.48rem;
                    margin-top:0.36rem;
                    .rig{
                        // border:1px solid red;
                        width:100%;
                        height:0.3rem;
                        margin-top:0.16rem;
                        color:rgb(7,17,27);
                        font-size:0.24rem;
                        line-height: 0.36rem;
                        .times{
                            display:inline-block;
                            margin-left:0.24rem;
                            font-size:0.24rem;
                            color:rgb(147,153,159);
                            line-height:0.36rem;
                        }
                        .star{
                            display:inline-block;
                            margin-left:0.24rem;
                            width:2rem;
                            // border:1px solid red;
                            height:0.3rem;
                            img{
                                vertical-align: top;
                                width:0.3rem; 
                                height:0.3rem; 
                            }
                        }
                        .score{
                            display:inline-block;
                            margin-left:0.24rem;
                            color:rgb(255,153,0);
                            font-size:0.24rem;
                        }

                     }
                }
            }
          
        }
        .whites{
            width:100%;
            height: 0.35rem;
            background-color: rgb(244,245,247);
        }
        .mids{
            width:100%;
            height:2.35rem;
            border:1px solid rgba(7,17,27,0.1);
            .one{
                // border:1px solid red;
                width:5rem;
                height:1.35rem;
                display: flex;
                div{
                    border:1px solid red;
                    border-radius: 0.04rem;
                    flex:1;
                    margin-top:0.36rem;
                    margin-left:0.16rem;
                    width:1.2rem;
                    height:0.6rem;
                }
                .all{
                    background-color: rgb(0,160,220);
                    .one{
                        font-size:0.24rem;
                        margin-top:0.15rem;
                        margin-left:0.15rem;
                    }
                }
                .fellgood{
                    background-color: rgb(206,234,247);
                    .one{
                        font-size:0.24rem;
                        margin-top:0.15rem;
                        margin-left:0.15rem;
                    }
                }
                .fellbad{
                    background-color: rgb(234,235,237);
                    .one{
                        font-size:0.24rem;
                        margin-top:0.15rem;
                        margin-left:0.15rem;
                    }
                }
            }
            .two{
                margin:0 auto;
                border-top:1px solid rgba(7,17,27,0.1);
                width:6.8rem;
                height:3rem;
               
                .trues{
                    display:inline-block;
                    border:1px solid rgb(176,179,180);
                    margin-left:0.4rem;
                    margin-top:0.14rem;
                    border-radius: 0.4rem;
                    width:0.4rem;
                    height:0.4rem;
                    background-color:rgb(176,179,184);
                    img{
                        width:0.36rem;
                        height:0.36rem;                                  
                    }
                }
                .secontent{
                    // border:1px solid red;
                    display:inline-block;
                    width:4rem;
                    height:0.4rem;
                    line-height: 0.36rem;
                    font-size: 0.24rem;
                    color:rgb(147,153,159);
                    margin-left:0.3rem;
                    margin-top:0.3rem;
                    
                }
            }
        }
        .bt{
            width:100%;
            height:100%;
            .rurn{
                margin:0 auto;
                border-bottom:1px solid rgba(7,17,27,0.1);
                width:6.8rem;
                height:3rem;
                .one{
                    border:1px solid red;
                    width:100%;
                    height:1rem;
                    .peoplepic{
                    margin-top:0.2rem;
                    display:inline-block;
                    border:1px solid red;
                    border-radius: 0.56rem;
                    width:0.56rem;
                    height:0.56rem;
                        img{
                            width:0.56rem;
                            height:0.56rem;
                        }
                }
                }
                .two{
                    border:1px solid red;
                    width:100%;
                    height:0.7rem;
                }
                .three{
                    border:1px solid red;
                    width:100%;
                    height:0.7rem;
                }
            }
        }
    }
</style>
