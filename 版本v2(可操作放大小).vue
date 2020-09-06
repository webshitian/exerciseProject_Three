<template>
    <div class="box5">
        <div class="box5_head">
            <div></div>
            <div class="box5_head_left">线网图</div>
            <div class="box5_head_right">
                <dv-border-box-7>
                    <router-link 
                      :to="{name:'stationMonitoringFirst'}" 
                      style="text-decoration:none;"
                      >
                        <span class="span">详情</span>
                    </router-link>    
                </dv-border-box-7>
            </div>
        </div>
        <div class="box5_content">
            <div id="box5_content">
                <SvgPanZoom
                    style="width: 100%; height:100%;"
                    :zoomEnabled="true"
                    :controlIconsEnabled="true"
                    :fit="true"
                    :center="true"
                >
                    <svg xmlns="http://www.w3.org/2000/svg" width='100%' height='100%' id='svg-id'> 
                       <g style="cursor:pointer"><line x1="-5" y1="-5" x2="55" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                       <g style="cursor:pointer" class="circleStyle"><circle cx="25" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="25" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">益田</text></g>
                       <g style="cursor:pointer"><line x1="35" y1="-5" x2="95" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                       <g style="cursor:pointer" class="circleStyle"><circle cx="65" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="65" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">石厦</text></g>
                       <g style="cursor:pointer"><line x1="75" y1="-5" x2="135" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                       <g style="cursor:pointer" class="circleStyle"><circle cx="105" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="105" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">购物公园</text></g>
                        <g style="cursor:pointer"><line x1="113.5" y1="-5" x2="173.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="143.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="143.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">福田</text></g>
                        <g style="cursor:pointer"><line x1="153.5" y1="-5" x2="213.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="183.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="183.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">少年宫</text></g>
                        <g style="cursor:pointer"><line x1="193.5" y1="-5" x2="253.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="223.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="223.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">莲花村</text></g>
                        <g style="cursor:pointer"><line x1="233.5" y1="-5" x2="293.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="263.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="263.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">华新</text></g>
                        <g style="cursor:pointer"><line x1="273.5" y1="-5" x2="333.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="303.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="303.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">通新岭</text></g>
                        <g style="cursor:pointer"><line x1="313.5" y1="-5" x2="373.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="343.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="343.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">红岭</text></g>
                        <g style="cursor:pointer"><line x1="353.5" y1="-5" x2="413.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="383.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="383.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">老街</text></g>
                        <g style="cursor:pointer"><line x1="393.5" y1="-5" x2="453.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="423.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="423.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">晒布</text></g>
                        <g style="cursor:pointer"><line x1="433.5" y1="-5" x2="493.5" y2="-5" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="463.5" cy="-5" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="463.5" y="25" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">翠竹</text></g>
                        <g style="cursor:pointer"><line x1="-6.5" y1="55" x2="53.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="23.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="23.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">田贝</text></g>
                        <g style="cursor:pointer"><line x1="33.5" y1="55" x2="93.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="63.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="63.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">水贝</text></g>
                        <g style="cursor:pointer"><line x1="73.5" y1="55" x2="133.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="103.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="103.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">草埔</text></g>
                        <g style="cursor:pointer"><line x1="113.5" y1="55" x2="173.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="143.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="143.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">布吉</text></g>
                        <g style="cursor:pointer"><line x1="153.5" y1="55" x2="213.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="183.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="183.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">木棉湾</text></g>
                        <g style="cursor:pointer"><line x1="193.5" y1="55" x2="253.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="223.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="223.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">大芬</text></g>
                        <g style="cursor:pointer"><line x1="233.5" y1="55" x2="293.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="263.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="263.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">丹竹头</text></g>
                        <g style="cursor:pointer"><line x1="273.5" y1="55" x2="333.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="303.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="303.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">六约</text></g>
                        <g style="cursor:pointer"><line x1="313.5" y1="55" x2="373.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="343.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="343.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">塘坑</text></g>
                        <g style="cursor:pointer"><line x1="353.5" y1="55" x2="413.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="383.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="383.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">横岗</text></g>
                        <g style="cursor:pointer"><line x1="393.5" y1="55" x2="453.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="423.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="423.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">永湖</text></g>
                        <g style="cursor:pointer"><line x1="433.5" y1="55" x2="493.5" y2="55" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="463.5" cy="55" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="463.5" y="85" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">荷坳</text></g>
                        <g style="cursor:pointer"><line x1="-6.5" y1="115" x2="53.5" y2="115" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="23.5" cy="115" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="23.5" y="145" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">大运</text></g>
                        <g style="cursor:pointer"><line x1="33.5" y1="115" x2="93.5" y2="115" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="63.5" cy="115" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="63.5" y="145" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">爱联</text></g>
                        <g style="cursor:pointer"><line x1="73.5" y1="115" x2="133.5" y2="115" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="103.5" cy="115" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="103.5" y="145" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">吉祥</text></g>
                        <g style="cursor:pointer"><line x1="113.5" y1="115" x2="173.5" y2="115" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="143.5" cy="115" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="143.5" y="145" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">龙城广场</text></g>
                        <g style="cursor:pointer"><line x1="153.5" y1="115" x2="213.5" y2="115" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="183.5" cy="115" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="183.5" y="145" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">南联</text></g>
                        <g style="cursor:pointer"><line x1="193.5" y1="115" x2="253.5" y2="115" stroke="#117cc5" stroke-width="4"></line></g>
                        <g style="cursor:pointer" class="circleStyle"><circle cx="223.5" cy="115" r="6" fill="#ffffff" stroke="#117cc5" stroke-width="3"></circle><text x="223.5" y="145" fill="white" font-size="12" text-anchor="middle" class="oTextStyle">双龙</text></g>
                    </svg>                  
                </SvgPanZoom>  
            </div>
        </div>
    </div>
</template>

<script>
import SvgPanZoom from "vue-svg-pan-zoom";
export default {
    data(){
      return{
        //   colour:'#FFFF00',
          colour:'#ff0000',
      }
    },
    components:{
        SvgPanZoom 
    },
    methods: {
        
        creatPublicSvg() {
            
            
            console.log('creatPublicSvg',this.colour)
            var circle = this.colour;
            var svgNS = 'http://www.w3.org/2000/svg';
            var oParent = document.getElementById('box5_content');
            var centerX = oParent.offsetWidth/2 - 250;
            var centerY = oParent.offsetHeight/2 - 70;
            var newSvg = '123';

            // var centerX = oParent.offsetWidth/2 - 350;
            // var centerY = oParent.offsetHeight/2 - 100;
            var website = [
                           '益田','石厦','购物公园','福田','少年宫','莲花村','华新','通新岭',
                           '红岭','老街','晒布','翠竹','田贝','水贝','草埔','布吉','木棉湾',
                           '大芬','丹竹头','六约','塘坑','横岗','永湖','荷坳','大运','爱联',
                           '吉祥','龙城广场','南联','双龙'
                           ];
                  
            var otherData = [];


            //封装一个创建标签的函数
            function createTag(tag,objAttr){
                
                var oTag = document.createElementNS(svgNS,tag);
                
                for(var attr in objAttr){
                    oTag.setAttribute(attr,objAttr[attr]);
                }
                
                return oTag;
            }

            for(var i = 0;i < website.length;i++){

                if(i <= 11){

                    var y = centerY;
                    var x = i * 40 + centerX;
                    otherData.push({ x:x, y:y, text:website[i]});

                }else if(i <= 23 ){

                        var x = i * 40 + centerX-480;
                        var y = centerY + 60;
                        otherData.push({ x:x, y:y, text:website[i]});
        
        
                }else if(i <= 35){
   
                        var x = i * 40 + centerX-960;
                        var y = centerY + 120;
                        otherData.push({ x:x, y:y, text:website[i]});
        
                }else if(i <= 47){
             
                        var x = i * 40 + centerX-1440;
                        var y = centerY + 180;
                        otherData.push({ x:x, y:y, text:website[i]});
             
                }
                                 
            }
            
            var data = {
                otherNode:otherData
            }    
  
            console.log(data)
            //  封装一个创建标签的方法
             function addTag(){
                var oSvg = document.getElementById('svg-id');
                // var oSvg = createTag('svg',{'xmlns':svgNS,'width':'100%','height':'100%','class':'svg-id'});

                for(var i = 0;i < data.otherNode.length;i++){
                    //把每一个数据传过去，并添加到svg当中
                    addOtherTag(data.otherNode[i] , oSvg);
                }                
                // oParent.appendChild(oSvg);
                // console.log('打印出了',oSvg);
                // console.log('打印出了2',oParent);
            }
            addTag()

            function addOtherTag(otherAttr , oSvg){

                var oG = createTag('g',{'style':'cursor:pointer'});
                var oLine1 = createTag('line',{'x1':otherAttr.x,'y1':otherAttr.y,'x2':otherAttr.x + 60,'y2':otherAttr.y ,'stroke':'#117cc5','stroke-width':'4'})
                
                oG.appendChild(oLine1);
                oSvg.appendChild(oG);

                // console.log('输出oG_1',oG)

                var oG = createTag('g',{'style':'cursor:pointer','class':'circleStyle'});
                var oCircle = createTag('circle',{'cx':otherAttr.x + 30,'cy':otherAttr.y,'r':'6','fill':'white','stroke':'#117cc5','stroke-width':'3','fill':'#ffffff'})
                var oText = createTag('text',{'x':otherAttr.x + 30,'y':otherAttr.y + 30,'fill':'white','font-size':'12','text-anchor':'middle','class':'oTextStyle'})
                oText.innerHTML = otherAttr.text;

                oG.appendChild(oCircle);
                oG.appendChild(oText);

                oSvg.appendChild(oG); 

                newSvg = oSvg
                // console.log('输出oG_2',oG)
                // console.log('输出svg',oSvg)
                
            }

            console.log('输出svg',newSvg)
            // bindTag();

            // //封装一个触发圆和线就会触发的方法
            // function bindTag(){

            //     //获取圆的元素
            //     var aCircle = document.getElementsByClassName('circleStyle');
            //     //获取文本的元素
            //     var oText = document.getElementsByClassName('oTextStyle')
            //     //给每一个圆循环加入鼠标移入事件和鼠标移出事件
            //     console.log('createTag123',circle)
            //     for(var i = 0;i < aCircle.length; i ++){

            //         // console.log('输出',aCircle[i].lastChild.innerHTML)

            //         if(aCircle[i].lastChild.innerHTML == '水贝'){
            //             var preaCircle = aCircle[i].firstChild;
            //             preaCircle.setAttribute('stroke',circle);
            //             preaCircle.setAttribute('fill',circle);
            //             // preaCircle.setAttribute('stroke','red');
            //             // preaCircle.setAttribute('fill','red');
            //             // preaCircle.setAttribute('stroke','#00ff00');
            //             // preaCircle.setAttribute('fill','#00ff00');
            //             // console.log('输出',aCircle[i].innerHTML)
            //         }

            //         aCircle[i].onmouseenter = function(){

            //             var preoText = this.lastChild.innerHTML;
                        
            //             var preaCircle = this.firstChild;

            //             preaCircle.setAttribute('stroke','blue');
            //             preaCircle.setAttribute('fill','blue');

            //             // console.log('输出的值',preoText)
            //             // console.log('输出的值',preaCircle)

            //             startMove(preaCircle, 6, 8)
                        
            //             if(this.lastChild.innerHTML == '水贝'){
            //                 var preaCircle = this.firstChild;
            //                 preaCircle.setAttribute('stroke',circle);
            //                 preaCircle.setAttribute('fill',circle);
            //                 // preaCircle.setAttribute('stroke','red');
            //                 // preaCircle.setAttribute('fill','red');
            //             }
                        

            //         };
                    
            //         aCircle[i].onmouseleave = function(){
            //             var preoText = this.lastChild.innerHTML;
                        
            //             var preaCircle = this.firstChild;

            //             preaCircle.setAttribute('stroke','#117cc5');
            //             preaCircle.setAttribute('fill','#ffffff');

            //             startMove(preaCircle, 8, 6)

            //             if(this.lastChild.innerHTML == '水贝'){
            //                 var preaCircle = this.firstChild;
            //                 preaCircle.setAttribute('stroke',circle);
            //                 preaCircle.setAttribute('fill',circle);
            //                 // preaCircle.setAttribute('stroke','red');
            //                 // preaCircle.setAttribute('fill','red');
                         
            //             }

            //         };

            //     }

            // }

            // // 封装触发后的效果(弹性的运动)
            // function startMove(obj,r1,r2){
            //     //存当前的r值是r1
            //     var nowR = r1;
            //     //鼠标移入的r值是r2
            //     var overR = r2;
            //     //存起始的速度
            //     obj.speed = 0;
            //     //运动的操作,清除旧的运动
            //     clearInterval(obj.timer);
            //     //开始一个新的运动
            //     obj.timer = setInterval(function(){

            //         //弹性公式
            //         obj.speed += (overR - nowR) / 6;
            //         //设置摩擦的系数,使圆的变化的速度慢下来
            //         obj.speed *= 0.9    ;
            //         //if是停止条件，什么时候停
            //         //满足两个条件停止，距离的绝对值小于等于1,然后是速度的绝对值小于等于1，说明它们是非常的近了，速度是非常的小
            //         if( Math.abs(overR - nowR) <=1 && Math.abs(obj.speed) <=1){
                        
            //             clearInterval(obj.timer);
            //             //把停止的值设置成指定的目标点
            //             obj.setAttribute('r',overR);
            //         }else{
                        
            //             //对nowR进行重新的赋值
            //             nowR += obj.speed;
            //             obj.setAttribute('r',nowR)
            //         }
            //     },30);
                
            // }        

  
    
            
        }
    },
    mounted(){
        // this.creatPublicSvg();
    }
}
</script>

<style scoped lang="less">
body{
    margin:0;
}
.box5{
    width:100%;
    height:14rem;
    background-color: transparent;
    // 盒子上部分
    .box5_head{
        display: flex;
        justify-content: space-between;
        padding:0.1rem 0.1rem;
        // border: 1px solid red;

        //标题的名字
        .box5_head_left{
            font-size:0.3rem;
            color: #fff;
            //标题是三个个字
            margin-left: 1.3rem;
            // margin-top:0.2rem;
        }
        //标题旁边两个按钮
        .box5_head_right{
            display: flex;         
            .span{
                display: block;
                color:#fff;
                width: 1rem;
                height: 0.45rem;
                text-align: center;
                line-height: 0.45rem;
                padding:0 0.1rem;
                // margin-left: 0.2rem;
                font-size:0.2rem;
            }
            // :first-child{
            //     margin-right:0.1rem;
            //     }     
            }
        }  
    //盒子内容部分
    .box5_content{
        display:flex;
        width: 98%;
        // width: 7.67rem;
        height: 2.8rem;
        color: #fff;
        // border: 1px solid red;
        font-size: 0.2rem;
        //设置地铁的图片
        // background:url(subway.jpg);
        background-size:100% 100%;
        // border: 1px solid red;
        padding: 0.05rem;
        #box5_content{
            width: 100%;
            height: 2.8rem;
            padding: 0 0.05rem;
        }
    }
}  

</style>