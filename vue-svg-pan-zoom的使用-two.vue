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
               <!-- <iframe src="../../../../static/txt.ftl" style="width:100%; height:100%" frameborder="no" border="0" marginwidth="0" marginheight="0" scrolling="no" allowTransparency="true"></iframe> -->
            </div>
        </div>
    </div>
</template>


<script>

export default {
    data(){
      return{
        
      }
    },
    components:{
        // svgPanZoom
    },
    methods: {
        
        creatPublicSvg() {
            console.log('输出',appendChild());
            // svgPanZoom();
            var svgNS = 'http://www.w3.org/2000/svg';
            var oParent = document.getElementById('box5_content');
            var centerX = oParent.offsetWidth/2 - 250;
            var centerY = oParent.offsetHeight/2 - 70;
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
  

             //封装一个创建标签的方法
             function addTag(){
                var oSvg = createTag('svg',{'xmlns':svgNS,'width':'100%','height':'100%','class':'svg-id'});

                for(var i = 0;i < data.otherNode.length;i++){
                    //把每一个数据传过去，并添加到svg当中
                    addOtherTag(data.otherNode[i] , oSvg);
                }                
                oParent.appendChild(oSvg);

            }
            addTag()

            function addOtherTag(otherAttr , oSvg){

                var oG = createTag('g',{'style':'cursor:pointer'});
                var oLine1 = createTag('line',{'x1':otherAttr.x,'y1':otherAttr.y,'x2':otherAttr.x + 60,'y2':otherAttr.y ,'stroke':'red'})
                
                oG.appendChild(oLine1);
                oSvg.appendChild(oG);


                var oG = createTag('g',{'style':'cursor:pointer','class':'circleStyle'});
                var oCircle = createTag('circle',{'cx':otherAttr.x + 30,'cy':otherAttr.y,'r':'6','fill':'white','stroke':'red','strole-width':'1','fill':'#ffffff'})
                var oText = createTag('text',{'x':otherAttr.x + 30,'y':otherAttr.y + 30,'fill':'white','font-size':'12','text-anchor':'middle','class':'oTextStyle'})
                oText.innerHTML = otherAttr.text;

                oG.appendChild(oCircle);
                oG.appendChild(oText);

                oSvg.appendChild(oG); 

                // console.log('输出oG',oG)
            }

            bindTag();

            //封装一个触发圆和线就会触发的方法
            function bindTag(){


                //获取圆的元素
                var aCircle = document.getElementsByClassName('circleStyle');
                //获取文本的元素
                var oText = document.getElementsByClassName('oTextStyle')
                //给每一个圆循环加入鼠标移入事件和鼠标移出事件
                for(var i = 0;i < aCircle.length; i ++){

                    aCircle[i].onmouseenter = function(){

                        var preoText = this.lastChild.innerHTML;
                        
                        var preaCircle = this.firstChild;

                        preaCircle.setAttribute('stroke','blue');
                        preaCircle.setAttribute('fill','blue');
  
                        console.log('输出的值',preoText)
                        console.log('输出的值',preaCircle)

                        startMove(preaCircle, 6, 8)

                    };
                      
                    aCircle[i].onmouseleave = function(){
                        var preoText = this.lastChild.innerHTML;
                        
                        var preaCircle = this.firstChild;

                        preaCircle.setAttribute('stroke','red');
                        preaCircle.setAttribute('fill','#ffffff');

                        startMove(preaCircle, 8, 6)
                    };


                }

            }

            //封装触发后的效果(弹性的运动)
            function startMove(obj,r1,r2){
                //存当前的r值是r1
                var nowR = r1;
                //鼠标移入的r值是r2
                var overR = r2;
                //存起始的速度
                obj.speed = 0;
                //运动的操作,清除旧的运动
                clearInterval(obj.timer);
                //开始一个新的运动
                obj.timer = setInterval(function(){

                    //弹性公式
                    obj.speed += (overR - nowR) / 6;
                    //设置摩擦的系数,使圆的变化的速度慢下来
                    obj.speed *= 0.9    ;
                    //if是停止条件，什么时候停
                    //满足两个条件停止，距离的绝对值小于等于1,然后是速度的绝对值小于等于1，说明它们是非常的近了，速度是非常的小
                    if( Math.abs(overR - nowR) <=1 && Math.abs(obj.speed) <=1){
                        
                        clearInterval(obj.timer);
                        //把停止的值设置成指定的目标点
                        obj.setAttribute('r',overR);
                    }else{
                        
                        //对nowR进行重新的赋值
                        nowR += obj.speed;
                        obj.setAttribute('r',nowR)
                    }
                },30);
                
            }        

            // window.panZoomInstance = svgPanZoom('#svg-id', {
            //     zoomEnabled: true,
            //     controlIconsEnabled: true,
            //     fit: true,
            //     center: true,
            //     minZoom: 0.1
            // });

            
            // Zoom out
            // 设置初始进入页面时线路图的大小
            // panZoomInstance.zoom(0.7);
            // panZoomInstance.zoom(0.2);
            // panZoomInstance.resize();
            // panZoomInstance.center();
            
            // function customPanBy(amount){ // {x: 1, y: 2}
            //     var animationTime = 300 // ms
            //         , animationStepTime = 15 // one frame per 30 ms
            //         , animationSteps = animationTime / animationStepTime
            //         , animationStep = 0
            //         , intervalID = null
            //         , stepX = amount.x / animationSteps
            //         , stepY = amount.y / animationSteps 

            //     intervalID = setInterval(function(){
            //             if (animationStep++ < animationSteps) {
            //             panZoomInstance.panBy({x: stepX, y: stepY})
            //             } else {
            //             // Cancel interval
            //             clearInterval(intervalID)
            //             }
            //         }, animationStepTime)

            // }      
            
        }
    },
    mounted(){
        
        this.creatPublicSvg();
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