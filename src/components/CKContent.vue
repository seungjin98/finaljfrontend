<template>
    <section class="content">
            <section class="left_content">
                <div class="sidecontent1">
                    <h1>Month Select</h1>
                    <div class="month_select">
                        <button id="jan" class="btn-style1" v-on:click="changeJan">Jan</button>
                        <button id="feb" class="btn-style1" v-on:click="changeFeb">Feb</button>
                        <button id="mar" class="btn-style1" v-on:click="changeMar">Mar</button>
                        <button id="apr" class="btn-style1" v-on:click="changeApr">Apr</button>
                        <button id="may" class="btn-style1" v-on:click="changeMay">May</button>
                        <button id="jun" class="btn-style1" v-on:click="changeJun">Jun</button>
                        <button id="jul" class="btn-style1" v-on:click="changeJul">Jul</button>
                        <button id="aug" class="btn-style1" v-on:click="changeAug">Aug</button>
                        <button id="sep" class="btn-style1" v-on:click="changeSep">Sep</button>
                        <button id="oct" class="btn-style1" v-on:click="changeOct">Oct</button>
                        <button id="nov" class="btn-style1" v-on:click="changeNov">Nov</button>
                        <button id="dec" class="btn-style1" v-on:click="changeDec">Dec</button>
                    </div>
                    <div class="sidecontent2">
                        <h1>Foreign visitors.</h1>
                        <div class="charts">
                            <span>Japan</span>
                            <div id="japen" class="charts__chart chart--p2 chart--grey" data-percent></div>
                            <!-- /.charts__chart -->
                            <span>USA</span>
                            <div id="usa" class="charts__chart chart--p21 chart--grey" data-percent></div>
                            <!-- /.charts__chart -->
                            <span>China</span>
                            <div id="china" class="charts__chart chart--p13 chart--grey" data-percent></div>
                            <!-- /.charts__chart -->
                            <span>Other Countries</span>
                            <div id="kor" class="charts__chart chart--p64 chart--grey" data-percent></div>
                            <!-- /.charts__chart -->
                        </div>
                    </div>
                </div>
            </section>
            <div class="mainimage">
                <!-- <img src="../image/제작자료1.png" alt="" usemap="#Map"> -->
                <img v-bind:src="mapSrc"/>
                <!-- <map name="Map" id="Map">
                    <area shape="poly" coords="146,41,99,88,110,127,137,111,153,135,139,146,110,143,118,205,170,204,205,177,206,132,184,119,183,94,191,83,164,61,141,36" href="gyung.html" alt="경기도" id="gyeonggido">
                </map> -->
                <div class="area" id="seoul">Seoul<br>
                    <button class="btn-style2"><a href="seoul.html">Move</a></button>
                </div>
                <div id="seoul_1"><img v-bind:src="redSrc" class="red" id="seoul_red" alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="gyeonggi">Gyeong<br>Gi
                    <button class="btn-style2"><a href="gyeonggi.html">Move</a></button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="gyeonggi_red"  alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="chungbuk">Chung<br>Buk
                    <button class="btn-style2" onclick="location.href='chungbuk.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="chungbuk_red"  alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="chungnam">Chung<br>Nam
                    <button class="btn-style2" onclick="location.href='chungnam.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="chungnam_red"  alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="jeollanam">Jeol<br>Nam
                    <button class="btn-style2" onclick="location.href='jeolnam.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="jeollanam_red"  alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="jeollabuk">Jeol<br>Buk
                    <button class="btn-style2" onclick="location.href='jeolbuk.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="jeollabuk_red" alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="gangwon">Gang<br>Won
                    <button class="btn-style2" onclick="location.href='gangwon.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="gangwon_red" alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="gyeongbuk">Gyeong<br>Buk
                    <button class="btn-style2" onclick="location.href='gyeongbuk.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="gyeongbuk_red" alt="" style="width: 8px; height: 8px;"></div>

                <div class="area" id="gyeongnam">Gyeong<br>Nam
                    <button class="btn-style2" onclick="location.href='gyeongnam.html';">Move</button>
                </div>
                <div><img v-bind:src="redSrc" class="red" id="gyeongnam_red" alt="" style="width: 8px; height: 8px;"></div>

                <svg width="100%" height="100%">
                    <line id="seoul_line" stroke="black"></line>
                    <line id="gyeonggi_line" stroke="black"></line>
                    <line id="chungbuk_line" stroke="black"></line>
                    <line id="chungnam_line" stroke="black"></line>
                    <line id="jeollabuk_line" stroke="black"></line>
                    <line id="jeollanam_line" stroke="black"></line>
                    <line id="gangwon_line" stroke="black"></line>
                    <line id="gyeongbuk_line" stroke="black"></line>
                    <line id="gyeongnam_line" stroke="black"></line>
                </svg>
            </div>
            <section class="right_content">


            </section>
        </section>
</template>

<script>
export default {
    
    data(){
        return {
            mapSrc : '../images/map.jpg',
            redSrc : '../images/red.png'

        }
        
    },
    methods : {
        
        changejan() {
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")

            japen.className = 'charts__chart chart--p16 chart--grey'
            usa.className = 'charts__chart chart--p6 chart--grey'
            china.className = 'charts__chart chart--p38 chart--grey'
            kor.className = 'charts__chart chart--p40 chart--grey'
        },
        changeFeb(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")

            japen.className = 'charts__chart chart--p30 chart--grey'
            usa.className = 'charts__chart chart--p6 chart--grey'
            china.className = 'charts__chart chart--p14 chart--grey'
            kor.className = 'charts__chart chart--p50 chart--grey'
        },
 
        changeMar(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")

            japen.className = 'charts__chart chart--p10 chart--grey'
            usa.className = 'charts__chart chart--p12 chart--grey'
            china.className = 'charts__chart chart--p20 chart--grey'
            kor.className = 'charts__chart chart--p58 chart--grey'
        },
        changeApr(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p1 chart--grey'
             usa.className = 'charts__chart chart--p22 chart--grey'
            china.className = 'charts__chart chart--p10 chart--grey'
             kor.className = 'charts__chart chart--p67 chart--grey'
        },
        changeMay(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p1 chart--grey'
            usa.className = 'charts__chart chart--p29 chart--grey'
            china.className = 'charts__chart chart--p17 chart--grey'
            kor.className = 'charts__chart chart--p53 chart--grey'
        },
        changeJun(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p1 chart--grey'
            usa.className = 'charts__chart chart--p27 chart--grey'
            china.className = 'charts__chart chart--p14 chart--grey'
            kor.className = 'charts__chart chart--p58 chart--grey'
        },
        changeJul(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p1 chart--grey'
            usa.className = 'charts__chart chart--p20 chart--grey'
            china.className = 'charts__chart chart--p15 chart--grey'
            kor.className = 'charts__chart chart--p64 chart--grey'
        },
        changeAug(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p2 chart--grey'
            usa.className = 'charts__chart chart--p21 chart--grey'
            china.className = 'charts__chart chart--p24 chart--grey'
            kor.className = 'charts__chart chart--p53 chart--grey'
        },
        changeSep(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            apen.className = 'charts__chart chart--p1 chart--grey'
            usa.className = 'charts__chart chart--p19 chart--grey'
            china.className = 'charts__chart chart--p23 chart--grey'
            kor.className = 'charts__chart chart--p57 chart--grey'
        },
        changeOct(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p2 chart--grey'
            usa.className = 'charts__chart chart--p20 chart--grey'
            china.className = 'charts__chart chart--p18 chart--grey'
            kor.className = 'charts__chart chart--p60 chart--grey'
        },changeNov(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p2 chart--grey'
            usa.className = 'charts__chart chart--p22 chart--grey'
            china.className = 'charts__chart chart--p15 chart--grey'
            kor.className = 'charts__chart chart--p61 chart--grey'
        },
        changeDec(){
            const japen = document.querySelector("#japen")
            const usa = document.querySelector("#usa")
            const china = document.querySelector("#china")
            const kor = document.querySelector("#kor")
            
            japen.className = 'charts__chart chart--p2 chart--grey'
            usa.className = 'charts__chart chart--p21 chart--grey'
            china.className = 'charts__chart chart--p13 chart--grey'
            kor.className = 'charts__chart chart--p64 chart--grey'
        }
    }
}
</script>

<style>

   * {
    margin: 0;
    padding: 0;
}

a {
    text-decoration: none;
    color: #fff;
}
a:hover {
    color:#000;
}

/* button style*/


button,
button::after {
    transition: all 1.0s;
}

button {
    background: none;
    width: 100px;
    padding: 10px;
    border: 3px solid #fff;
    border-radius: 10px;
    color: #fff;
    display: block;
    position: relative;
    text-transform: uppercase;
    z-index: 1;
    margin: 0 auto;
    margin-top: 10px;
    font-family: 'Mochiy Pop P One', sans-serif;
    cursor: pointer;
}

button::before,
button::after {
    background: #fff;
    content: '';
    position: absolute;
    z-index: -1;
}

button:hover {
    color: #000;
}

.btn-style1::after {
    height: 0;
    left: 0;
    top: 0;
    width: 100%;
}

.btn-style1:hover:after {
    height: 100%;
}

.btn-style2::after {
    height: 0;
    left: 50%;
    top: 50%;
    width: 0;
}

.btn-style2:hover:after {
    height: 100%;
    left: 0;
    top: 0;
    width: 100%;
}
/* content */

.content {
    display: flex;
    flex-flow: row nowrap;
    justify-content: center;
    width: 100%;
    margin: 0 auto;
    background-color: #fff;
    z-index: -2;
}


/* 왼쪽사이드 내용 */

.left_content {
    order: 1;
    display: flex;
    flex-flow: column;
    width: 20%;
    background-color: #423F3E;
    color: white;
}

.sidecontent1 {
    padding-top: 50px;
    display: block;
    text-align: center;
    font-family: 'Mochiy Pop P One', sans-serif;
}

.sidecontent1 h1 {
    margin: 20px;
}

.month_select {
    display: flex;
    width: 100%;
    flex-flow: row wrap;
}

.month_select div {
    box-sizing: border-box;
    padding: 10px 10px;
    margin: 2%;
    width: 29%;
    border: 1px solid white;
    cursor: pointer;
}

.month_select div a {
    text-decoration: none;
    color: white;
}


/* 중앙 이미지  */

.mainimage {
    order: 2;
    width: 60%;
    height: 1000px;
    background-color: #423F3E;
    position: relative;
    z-index: 0;
}

.mainimage img {
    position: absolute;
    top: 0;
    left: 50%;
    transform: translate(-50%, 0);
    display: block;
    width: 50%;
    margin: 0 auto;
    justify-content: center;
    z-index: -1;
}

.area {
    position: absolute;
    border: 2px solid #2b2020;
    border-radius: 10px;
    box-sizing: border-box;
    font-size: 30px;
    padding: 10px;
    color: white;
    background-color: #2b2020;
    width: 150px;
    font-family: 'Mochiy Pop P One', sans-serif;
    font-size: 20px;
}

.area button {
    padding: 5px;
    margin-top: 20px;
}

.red {
    position: absolute;
    top: 0;
}

#seoul {
    top: 50px;
    left: 450px;
}

#seoul_red {
    top: 470px;
    left: 530px;
}

#gyeonggi {
    top: 65px;
    right: 250px;
}

#gyeonggi_red {
    top: 450px;
    left: 520px;
}

#chungbuk {
    top: 50px;
    left: 200px;
}

#chungbuk_red {
    top: 530px;
    left: 570px;
}

#chungnam {
    top: 250px;
    left: 150px;
}

#chungnam_red {
    top: 540px;
    left: 530px;
}

#jeollanam {
    top: 650px;
    left: 250px;
}

#jeollanam_red {
    top: 680px;
    left: 530px;
}

#jeollabuk {
    top: 450px;
    left: 150px;
}

#jeollabuk_red {
    top: 610px;
    left: 550px;
}

#gangwon {
    top: 250px;
    right: 200px;
}

#gangwon_red {
    top: 480px;
    left: 620px;
}

#gyeongbuk {
    right: 200px;
    top: 450px;
}

#gyeongbuk_red {
    top: 560px;
    left: 630px;
}

#gyeongnam {
    top: 650px;
    right: 300px;
}

#gyeongnam_red {
    top: 630px;
    left: 630px;
}

line {
    z-index: 10;
    position: absolute;
    left: 100px;
}


/* 오른쪽 사이드 내용 */

.right_content {
    order: 3;
    display: flex;
    flex-flow: column;
    width: 20%;
    background-color: #423F3E;
    color: white;
}

.sidecontent2 {
    padding: 10px 5%;
    margin-top: 100px;
}

.sidecontent2 h1 {
    font-family: 'Mochiy Pop P One', sans-serif;
}


.charts{font-size:10px}.charts span{text-transform:uppercase}.charts--vertical{height:25rem;display:inline-block}.charts--vertical .charts__percent{display:table;position:relative;top:50%;-webkit-transform:rotate(-90deg);-ms-transform:rotate(-90deg);transform:rotate(-90deg);left:-.5rem;color:#ebeded}.charts--vertical .charts__percent:empty::after{content:"100%";margin-left:.345rem;font-size:1.1rem}.charts--vertical .charts__chart{width:2rem;height:100%;display:inline-block;margin:0 .2rem}.charts--vertical .charts__chart>.charts__chart{width:100%}.charts--vertical.charts--grouped::after{content:"Oops! Seems that you used 'charts--grouped' in 'charts--vertical'. This isn't supported.";font-size:2rem;color:#D0716F}.charts--vertical.charts--grouped .charts__chart{display:none}.charts__chart[data-percent]::after{content:attr(data-percent);display:block;margin-left:45%;position:relative;color:#ebeded;font-size:1.2em;top:.21em}.charts.charts--vertical .chart--p0 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p0[data-percent]::after{content:"0%"}.charts__chart{background-color:#7f8c8d;width:100%;height:2em;margin:.5em 0}.charts__chart.chart--hover:hover{background-color:#727f80}.charts__chart>.charts__chart{height:100%}.chart--xs{height:.5em}.chart--xs[data-percent]::after{top:-.4em;margin-left:calc(100% + .3em);color:#667273}.chart--sm{height:1em}.chart--sm[data-percent]::after{top:-.25em;margin-left:calc(100% + .3em);color:#667273}.charts--vertical .chart--sm .charts__percent,.charts--vertical .chart--xs .charts__percent{left:-2.2rem;color:#333}.chart--lg{height:3em}.chart--lg[data-percent]::after{font-size:1.4em;top:.33em}.chart--xl{height:4.5em}.chart--xl[data-percent]::after{font-size:2em;top:.4em}.charts--vertical .chart--xs{width:.5em;margin-left:1.5rem}.charts--vertical .chart--sm{width:1em;margin-left:1.4rem}.charts--vertical .chart--lg{width:3em}.charts--vertical .chart--lg .charts__percent{left:0}.charts--vertical .chart--xl{width:4.5em}.charts--vertical .chart--xl .charts__percent{left:.75em}.charts:not(.charts--vertical) .chart--p0{width:0}.charts.charts--vertical .chart--p0{height:0%}.charts.charts--vertical .chart--p1 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p1[data-percent]::after{content:"1%"}.charts:not(.charts--vertical) .chart--p1{width:1%}.charts.charts--vertical .chart--p1{height:1%}.charts.charts--vertical .chart--p2 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p2[data-percent]::after{content:"2%"}.charts:not(.charts--vertical) .chart--p2{width:2%}.charts.charts--vertical .chart--p2{height:2%}.charts.charts--vertical .chart--p3 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p3[data-percent]::after{content:"3%"}.charts:not(.charts--vertical) .chart--p3{width:3%}.charts.charts--vertical .chart--p3{height:3%}.charts.charts--vertical .chart--p4 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p4[data-percent]::after{content:"4%"}.charts:not(.charts--vertical) .chart--p4{width:4%}.charts.charts--vertical .chart--p4{height:4%}.charts.charts--vertical .chart--p5 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p5[data-percent]::after{content:"5%"}.charts:not(.charts--vertical) .chart--p5{width:5%}.charts.charts--vertical .chart--p5{height:5%}.charts.charts--vertical .chart--p6 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p6[data-percent]::after{content:"6%"}.charts:not(.charts--vertical) .chart--p6{width:6%}.charts.charts--vertical .chart--p6{height:6%}.charts.charts--vertical .chart--p7 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p7[data-percent]::after{content:"7%"}.charts:not(.charts--vertical) .chart--p7{width:7%}.charts.charts--vertical .chart--p7{height:7%}.charts.charts--vertical .chart--p8 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p8[data-percent]::after{content:"8%"}.charts:not(.charts--vertical) .chart--p8{width:8%}.charts.charts--vertical .chart--p8{height:8%}.charts.charts--vertical .chart--p9 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p9[data-percent]::after{content:"9%"}.charts:not(.charts--vertical) .chart--p9{width:9%}.charts.charts--vertical .chart--p9{height:9%}.charts.charts--vertical .chart--p10 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p10[data-percent]::after{content:"10%"}.charts:not(.charts--vertical) .chart--p10{width:10%}.charts.charts--vertical .chart--p10{height:10%}.charts.charts--vertical .chart--p11 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p11[data-percent]::after{content:"11%"}.charts:not(.charts--vertical) .chart--p11{width:11%}.charts.charts--vertical .chart--p11{height:11%}.charts.charts--vertical .chart--p12 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p12[data-percent]::after{content:"12%"}.charts:not(.charts--vertical) .chart--p12{width:12%}.charts.charts--vertical .chart--p12{height:12%}.charts.charts--vertical .chart--p13 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p13[data-percent]::after{content:"13%"}.charts:not(.charts--vertical) .chart--p13{width:13%}.charts.charts--vertical .chart--p13{height:13%}.charts.charts--vertical .chart--p14 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p14[data-percent]::after{content:"14%"}.charts:not(.charts--vertical) .chart--p14{width:14%}.charts.charts--vertical .chart--p14{height:14%}.charts.charts--vertical .chart--p15 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p15[data-percent]::after{content:"15%"}.charts:not(.charts--vertical) .chart--p15{width:15%}.charts.charts--vertical .chart--p15{height:15%}.charts.charts--vertical .chart--p16 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p16[data-percent]::after{content:"16%"}.charts:not(.charts--vertical) .chart--p16{width:16%}.charts.charts--vertical .chart--p16{height:16%}.charts.charts--vertical .chart--p17 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p17[data-percent]::after{content:"17%"}.charts:not(.charts--vertical) .chart--p17{width:17%}.charts.charts--vertical .chart--p17{height:17%}.charts.charts--vertical .chart--p18 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p18[data-percent]::after{content:"18%"}.charts:not(.charts--vertical) .chart--p18{width:18%}.charts.charts--vertical .chart--p18{height:18%}.charts.charts--vertical .chart--p19 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p19[data-percent]::after{content:"19%"}.charts:not(.charts--vertical) .chart--p19{width:19%}.charts.charts--vertical .chart--p19{height:19%}.charts.charts--vertical .chart--p20 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p20[data-percent]::after{content:"20%"}.charts:not(.charts--vertical) .chart--p20{width:20%}.charts.charts--vertical .chart--p20{height:20%}.charts.charts--vertical .chart--p21 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p21[data-percent]::after{content:"21%"}.charts:not(.charts--vertical) .chart--p21{width:21%}.charts.charts--vertical .chart--p21{height:21%}.charts.charts--vertical .chart--p22 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p22[data-percent]::after{content:"22%"}.charts:not(.charts--vertical) .chart--p22{width:22%}.charts.charts--vertical .chart--p22{height:22%}.charts.charts--vertical .chart--p23 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p23[data-percent]::after{content:"23%"}.charts:not(.charts--vertical) .chart--p23{width:23%}.charts.charts--vertical .chart--p23{height:23%}.charts.charts--vertical .chart--p24 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p24[data-percent]::after{content:"24%"}.charts:not(.charts--vertical) .chart--p24{width:24%}.charts.charts--vertical .chart--p24{height:24%}.charts.charts--vertical .chart--p25 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p25[data-percent]::after{content:"25%"}.charts:not(.charts--vertical) .chart--p25{width:25%}.charts.charts--vertical .chart--p25{height:25%}.charts.charts--vertical .chart--p26 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p26[data-percent]::after{content:"26%"}.charts:not(.charts--vertical) .chart--p26{width:26%}.charts.charts--vertical .chart--p26{height:26%}.charts.charts--vertical .chart--p27 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p27[data-percent]::after{content:"27%"}.charts:not(.charts--vertical) .chart--p27{width:27%}.charts.charts--vertical .chart--p27{height:27%}.charts.charts--vertical .chart--p28 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p28[data-percent]::after{content:"28%"}.charts:not(.charts--vertical) .chart--p28{width:28%}.charts.charts--vertical .chart--p28{height:28%}.charts.charts--vertical .chart--p29 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p29[data-percent]::after{content:"29%"}.charts:not(.charts--vertical) .chart--p29{width:29%}.charts.charts--vertical .chart--p29{height:29%}.charts.charts--vertical .chart--p30 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p30[data-percent]::after{content:"30%"}.charts:not(.charts--vertical) .chart--p30{width:30%}.charts.charts--vertical .chart--p30{height:30%}.charts.charts--vertical .chart--p31 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p31[data-percent]::after{content:"31%"}.charts:not(.charts--vertical) .chart--p31{width:31%}.charts.charts--vertical .chart--p31{height:31%}.charts.charts--vertical .chart--p32 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p32[data-percent]::after{content:"32%"}.charts:not(.charts--vertical) .chart--p32{width:32%}.charts.charts--vertical .chart--p32{height:32%}.charts.charts--vertical .chart--p33 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p33[data-percent]::after{content:"33%"}.charts:not(.charts--vertical) .chart--p33{width:33%}.charts.charts--vertical .chart--p33{height:33%}.charts.charts--vertical .chart--p34 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p34[data-percent]::after{content:"34%"}.charts:not(.charts--vertical) .chart--p34{width:34%}.charts.charts--vertical .chart--p34{height:34%}.charts.charts--vertical .chart--p35 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p35[data-percent]::after{content:"35%"}.charts:not(.charts--vertical) .chart--p35{width:35%}.charts.charts--vertical .chart--p35{height:35%}.charts.charts--vertical .chart--p36 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p36[data-percent]::after{content:"36%"}.charts:not(.charts--vertical) .chart--p36{width:36%}.charts.charts--vertical .chart--p36{height:36%}.charts.charts--vertical .chart--p37 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p37[data-percent]::after{content:"37%"}.charts:not(.charts--vertical) .chart--p37{width:37%}.charts.charts--vertical .chart--p37{height:37%}.charts.charts--vertical .chart--p38 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p38[data-percent]::after{content:"38%"}.charts:not(.charts--vertical) .chart--p38{width:38%}.charts.charts--vertical .chart--p38{height:38%}.charts.charts--vertical .chart--p39 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p39[data-percent]::after{content:"39%"}.charts:not(.charts--vertical) .chart--p39{width:39%}.charts.charts--vertical .chart--p39{height:39%}.charts.charts--vertical .chart--p40 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p40[data-percent]::after{content:"40%"}.charts:not(.charts--vertical) .chart--p40{width:40%}.charts.charts--vertical .chart--p40{height:40%}.charts.charts--vertical .chart--p41 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p41[data-percent]::after{content:"41%"}.charts:not(.charts--vertical) .chart--p41{width:41%}.charts.charts--vertical .chart--p41{height:41%}.charts.charts--vertical .chart--p42 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p42[data-percent]::after{content:"42%"}.charts:not(.charts--vertical) .chart--p42{width:42%}.charts.charts--vertical .chart--p42{height:42%}.charts.charts--vertical .chart--p43 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p43[data-percent]::after{content:"43%"}.charts:not(.charts--vertical) .chart--p43{width:43%}.charts.charts--vertical .chart--p43{height:43%}.charts.charts--vertical .chart--p44 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p44[data-percent]::after{content:"44%"}.charts:not(.charts--vertical) .chart--p44{width:44%}.charts.charts--vertical .chart--p44{height:44%}.charts.charts--vertical .chart--p45 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p45[data-percent]::after{content:"45%"}.charts:not(.charts--vertical) .chart--p45{width:45%}.charts.charts--vertical .chart--p45{height:45%}.charts.charts--vertical .chart--p46 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p46[data-percent]::after{content:"46%"}.charts:not(.charts--vertical) .chart--p46{width:46%}.charts.charts--vertical .chart--p46{height:46%}.charts.charts--vertical .chart--p47 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p47[data-percent]::after{content:"47%"}.charts:not(.charts--vertical) .chart--p47{width:47%}.charts.charts--vertical .chart--p47{height:47%}.charts.charts--vertical .chart--p48 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p48[data-percent]::after{content:"48%"}.charts:not(.charts--vertical) .chart--p48{width:48%}.charts.charts--vertical .chart--p48{height:48%}.charts.charts--vertical .chart--p49 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p49[data-percent]::after{content:"49%"}.charts:not(.charts--vertical) .chart--p49{width:49%}.charts.charts--vertical .chart--p49{height:49%}.charts.charts--vertical .chart--p50 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p50[data-percent]::after{content:"50%"}.charts:not(.charts--vertical) .chart--p50{width:50%}.charts.charts--vertical .chart--p50{height:50%}.charts.charts--vertical .chart--p51 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p51[data-percent]::after{content:"51%"}.charts:not(.charts--vertical) .chart--p51{width:51%}.charts.charts--vertical .chart--p51{height:51%}.charts.charts--vertical .chart--p52 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p52[data-percent]::after{content:"52%"}.charts:not(.charts--vertical) .chart--p52{width:52%}.charts.charts--vertical .chart--p52{height:52%}.charts.charts--vertical .chart--p53 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p53[data-percent]::after{content:"53%"}.charts:not(.charts--vertical) .chart--p53{width:53%}.charts.charts--vertical .chart--p53{height:53%}.charts.charts--vertical .chart--p54 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p54[data-percent]::after{content:"54%"}.charts:not(.charts--vertical) .chart--p54{width:54%}.charts.charts--vertical .chart--p54{height:54%}.charts.charts--vertical .chart--p55 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p55[data-percent]::after{content:"55%"}.charts:not(.charts--vertical) .chart--p55{width:55%}.charts.charts--vertical .chart--p55{height:55%}.charts.charts--vertical .chart--p56 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p56[data-percent]::after{content:"56%"}.charts:not(.charts--vertical) .chart--p56{width:56%}.charts.charts--vertical .chart--p56{height:56%}.charts.charts--vertical .chart--p57 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p57[data-percent]::after{content:"57%"}.charts:not(.charts--vertical) .chart--p57{width:57%}.charts.charts--vertical .chart--p57{height:57%}.charts.charts--vertical .chart--p58 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p58[data-percent]::after{content:"58%"}.charts:not(.charts--vertical) .chart--p58{width:58%}.charts.charts--vertical .chart--p58{height:58%}.charts.charts--vertical .chart--p59 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p59[data-percent]::after{content:"59%"}.charts:not(.charts--vertical) .chart--p59{width:59%}.charts.charts--vertical .chart--p59{height:59%}.charts.charts--vertical .chart--p60 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p60[data-percent]::after{content:"60%"}.charts:not(.charts--vertical) .chart--p60{width:60%}.charts.charts--vertical .chart--p60{height:60%}.charts.charts--vertical .chart--p61 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p61[data-percent]::after{content:"61%"}.charts:not(.charts--vertical) .chart--p61{width:61%}.charts.charts--vertical .chart--p61{height:61%}.charts.charts--vertical .chart--p62 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p62[data-percent]::after{content:"62%"}.charts:not(.charts--vertical) .chart--p62{width:62%}.charts.charts--vertical .chart--p62{height:62%}.charts.charts--vertical .chart--p63 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p63[data-percent]::after{content:"63%"}.charts:not(.charts--vertical) .chart--p63{width:63%}.charts.charts--vertical .chart--p63{height:63%}.charts.charts--vertical .chart--p64 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p64[data-percent]::after{content:"64%"}.charts:not(.charts--vertical) .chart--p64{width:64%}.charts.charts--vertical .chart--p64{height:64%}.charts.charts--vertical .chart--p65 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p65[data-percent]::after{content:"65%"}.charts:not(.charts--vertical) .chart--p65{width:65%}.charts.charts--vertical .chart--p65{height:65%}.charts.charts--vertical .chart--p66 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p66[data-percent]::after{content:"66%"}.charts:not(.charts--vertical) .chart--p66{width:66%}.charts.charts--vertical .chart--p66{height:66%}.charts.charts--vertical .chart--p67 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p67[data-percent]::after{content:"67%"}.charts:not(.charts--vertical) .chart--p67{width:67%}.charts.charts--vertical .chart--p67{height:67%}.charts.charts--vertical .chart--p68 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p68[data-percent]::after{content:"68%"}.charts:not(.charts--vertical) .chart--p68{width:68%}.charts.charts--vertical .chart--p68{height:68%}.charts.charts--vertical .chart--p69 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p69[data-percent]::after{content:"69%"}.charts:not(.charts--vertical) .chart--p69{width:69%}.charts.charts--vertical .chart--p69{height:69%}.charts.charts--vertical .chart--p70 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p70[data-percent]::after{content:"70%"}.charts:not(.charts--vertical) .chart--p70{width:70%}.charts.charts--vertical .chart--p70{height:70%}.charts.charts--vertical .chart--p71 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p71[data-percent]::after{content:"71%"}.charts:not(.charts--vertical) .chart--p71{width:71%}.charts.charts--vertical .chart--p71{height:71%}.charts.charts--vertical .chart--p72 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p72[data-percent]::after{content:"72%"}.charts:not(.charts--vertical) .chart--p72{width:72%}.charts.charts--vertical .chart--p72{height:72%}.charts.charts--vertical .chart--p73 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p73[data-percent]::after{content:"73%"}.charts:not(.charts--vertical) .chart--p73{width:73%}.charts.charts--vertical .chart--p73{height:73%}.charts.charts--vertical .chart--p74 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p74[data-percent]::after{content:"74%"}.charts:not(.charts--vertical) .chart--p74{width:74%}.charts.charts--vertical .chart--p74{height:74%}.charts.charts--vertical .chart--p75 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p75[data-percent]::after{content:"75%"}.charts:not(.charts--vertical) .chart--p75{width:75%}.charts.charts--vertical .chart--p75{height:75%}.charts.charts--vertical .chart--p76 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p76[data-percent]::after{content:"76%"}.charts:not(.charts--vertical) .chart--p76{width:76%}.charts.charts--vertical .chart--p76{height:76%}.charts.charts--vertical .chart--p77 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p77[data-percent]::after{content:"77%"}.charts:not(.charts--vertical) .chart--p77{width:77%}.charts.charts--vertical .chart--p77{height:77%}.charts.charts--vertical .chart--p78 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p78[data-percent]::after{content:"78%"}.charts:not(.charts--vertical) .chart--p78{width:78%}.charts.charts--vertical .chart--p78{height:78%}.charts.charts--vertical .chart--p79 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p79[data-percent]::after{content:"79%"}.charts:not(.charts--vertical) .chart--p79{width:79%}.charts.charts--vertical .chart--p79{height:79%}.charts.charts--vertical .chart--p80 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p80[data-percent]::after{content:"80%"}.charts:not(.charts--vertical) .chart--p80{width:80%}.charts.charts--vertical .chart--p80{height:80%}.charts.charts--vertical .chart--p81 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p81[data-percent]::after{content:"81%"}.charts:not(.charts--vertical) .chart--p81{width:81%}.charts.charts--vertical .chart--p81{height:81%}.charts.charts--vertical .chart--p82 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p82[data-percent]::after{content:"82%"}.charts:not(.charts--vertical) .chart--p82{width:82%}.charts.charts--vertical .chart--p82{height:82%}.charts.charts--vertical .chart--p83 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p83[data-percent]::after{content:"83%"}.charts:not(.charts--vertical) .chart--p83{width:83%}.charts.charts--vertical .chart--p83{height:83%}.charts.charts--vertical .chart--p84 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p84[data-percent]::after{content:"84%"}.charts:not(.charts--vertical) .chart--p84{width:84%}.charts.charts--vertical .chart--p84{height:84%}.charts.charts--vertical .chart--p85 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p85[data-percent]::after{content:"85%"}.charts:not(.charts--vertical) .chart--p85{width:85%}.charts.charts--vertical .chart--p85{height:85%}.charts.charts--vertical .chart--p86 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p86[data-percent]::after{content:"86%"}.charts:not(.charts--vertical) .chart--p86{width:86%}.charts.charts--vertical .chart--p86{height:86%}.charts.charts--vertical .chart--p87 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p87[data-percent]::after{content:"87%"}.charts:not(.charts--vertical) .chart--p87{width:87%}.charts.charts--vertical .chart--p87{height:87%}.charts.charts--vertical .chart--p88 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p88[data-percent]::after{content:"88%"}.charts:not(.charts--vertical) .chart--p88{width:88%}.charts.charts--vertical .chart--p88{height:88%}.charts.charts--vertical .chart--p89 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p89[data-percent]::after{content:"89%"}.charts:not(.charts--vertical) .chart--p89{width:89%}.charts.charts--vertical .chart--p89{height:89%}.charts.charts--vertical .chart--p90 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p90[data-percent]::after{content:"90%"}.charts:not(.charts--vertical) .chart--p90{width:90%}.charts.charts--vertical .chart--p90{height:90%}.charts.charts--vertical .chart--p91 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p91[data-percent]::after{content:"91%"}.charts:not(.charts--vertical) .chart--p91{width:91%}.charts.charts--vertical .chart--p91{height:91%}.charts.charts--vertical .chart--p92 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p92[data-percent]::after{content:"92%"}.charts:not(.charts--vertical) .chart--p92{width:92%}.charts.charts--vertical .chart--p92{height:92%}.charts.charts--vertical .chart--p93 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p93[data-percent]::after{content:"93%"}.charts:not(.charts--vertical) .chart--p93{width:93%}.charts.charts--vertical .chart--p93{height:93%}.charts.charts--vertical .chart--p94 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p94[data-percent]::after{content:"94%"}.charts:not(.charts--vertical) .chart--p94{width:94%}.charts.charts--vertical .chart--p94{height:94%}.charts.charts--vertical .chart--p95 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p95[data-percent]::after{content:"95%"}.charts:not(.charts--vertical) .chart--p95{width:95%}.charts.charts--vertical .chart--p95{height:95%}.charts.charts--vertical .chart--p96 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p96[data-percent]::after{content:"96%"}.charts:not(.charts--vertical) .chart--p96{width:96%}.charts.charts--vertical .chart--p96{height:96%}.charts.charts--vertical .chart--p97 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p97[data-percent]::after{content:"97%"}.charts:not(.charts--vertical) .chart--p97{width:97%}.charts.charts--vertical .chart--p97{height:97%}.charts.charts--vertical .chart--p98 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p98[data-percent]::after{content:"98%"}.charts:not(.charts--vertical) .chart--p98{width:98%}.charts.charts--vertical .chart--p98{height:98%}.charts.charts--vertical .chart--p99 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p99[data-percent]::after{content:"99%"}.charts:not(.charts--vertical) .chart--p99{width:99%}.charts.charts--vertical .chart--p99{height:99%}.charts.charts--vertical .chart--p100 .charts__percent:empty::after,.charts:not(.charts--vertical) .chart--p100[data-percent]::after{content:"100%"}.charts:not(.charts--vertical) .chart--p100{width:100%}.charts.charts--vertical .chart--p100{height:100%}.chart--default{background-color:#7f8c8d}.chart--default.chart--hover:hover{background-color:#727f80}.chart--blue{background-color:#2980b9}.chart--blue.chart--hover:hover{background-color:#2472a4}.chart--green{background-color:#27ae60}.chart--green.chart--hover:hover{background-color:#295}.chart--red{background-color:#c0392b}.chart--red.chart--hover:hover{background-color:#ab3326}.chart--yellow{background-color:#f1c40f}.chart--yellow.chart--hover:hover{background-color:#dab10d}.chart--grey{background-color:#362222}.chart--grey.chart--hover:hover{background-color:#233140}.chart--inverse{background-color:#ecf0f1}.chart--inverse.chart--hover:hover{background-color:#dde4e6}.charts--grouped [data-percent]::after{display:none}
</style>