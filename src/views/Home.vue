<template>
        <div class="test">
                <!-- <div class="test1">
                        <input type="checkbox" />
                </div>
                <div class="test2">
                        <img
                                src="../assets/img/111.jpg"
                                width="500px"
                                height="300px"
                        />
                        <p>hello world</p>
                        <p>welcome to my city!</p>
                        <h2>ChengDu</h2>
                </div>
                <div class="test3">
                        <img
                                src="../assets/img/风铃.jpg"
                                width="500px"
                                height="275px"
                        />
                </div> -->
                <div class="test4">
                        <div class="plane1">上</div>
                        <div class="plane2">下</div>
                        <div class="plane3">左</div>
                        <div class="plane4">右</div>
                        <div class="plane6">后</div>
                        <div class="plane5">前</div>
                </div>
                <div class="test55">
                        <div class="test5">
                                <div class="box1">菜单</div>
                                <div class="box2">菜单</div>
                        </div>
                        <div class="test5">
                                <div class="box1">视频</div>
                                <div class="box2">视频</div>
                        </div>
                        <div class="test5">
                                <div class="box1">主页</div>
                                <div class="box2">主页</div>
                        </div>
                        <div class="test5">
                                <div class="box1">资讯</div>
                                <div class="box2">资讯</div>
                        </div>
                        <div class="test5">
                                <div class="box1">详情</div>
                                <div class="box2">详情</div>
                        </div>
                        <div class="test5">
                                <div class="box1">更多</div>
                                <div class="box2">更多</div>
                        </div>
                </div>
                <div class="test6">
                        <div class="test61">
                                <div></div>
                                <div></div>
                                <div></div>
                                <div></div>
                        </div>
                        <div class="test62">
                                <div></div>
                                <div></div>
                                <div></div>
                                <div></div>
                        </div>
                </div>
                <div class="test7">
                        <div class="test71">
                                <ul>
                                        <li>
                                                <img
                                                        src="../assets/img/1.jpg"
                                                />
                                        </li>
                                        <li>
                                                <img
                                                        src="../assets/img/2.jpg"
                                                />
                                        </li>
                                        <li>
                                                <img
                                                        src="../assets/img/3.jpg"
                                                />
                                        </li>
                                        <li>
                                                <img
                                                        src="../assets/img/4.jpg"
                                                />
                                        </li>
                                        <li>
                                                <img
                                                        src="../assets/img/5.jpg"
                                                />
                                        </li>
                                        <li>
                                                <img
                                                        src="../assets/img/6.jpg"
                                                />
                                        </li>
                                </ul>
                        </div>
                </div>
                <div class="test8">
                        <div class="test81"></div>
                </div>
                <div class="test9">
                        <div class="box91">移入翻页</div>
                        <div class="box944">bye</div>
                        <div class="box94">第三页</div>
                        <div class="box933">world</div>
                        <div class="box93">第二页</div>
                        <div class="box922">hello</div>
                        <div class="box92">第一页</div>
                </div>
        </div>
</template>

<script>
export default {
        data() {
                return {};
        },
};
</script>

<style lang="less" scoped>
@keyframes rotate2 {
        0% {
                transform: rotateX(30deg) rotateY(180deg);
        }
        100% {
                transform: rotateX(30deg) rotateY(0);
        }
}
@keyframes rotate {
        0% {
                transform: rotateX(30deg) rotateY(0);
        }
        100% {
                transform: rotateX(30deg) rotateY(-180deg);
        }
}
.test9:hover .box944 {
        z-index: 50;
        animation: rotate2 2s 4s linear;
        animation-fill-mode: forwards; /*保持结束位置*/
}
.test9:hover .box94 {
        animation: rotate 2s 4s linear;
        animation-fill-mode: forwards; /*保持结束位置*/
        backface-visibility: hidden;
}
.test9:hover .box933 {
        z-index: 40;
        animation: rotate2 2s 2s linear;
        animation-fill-mode: forwards; /*保持结束位置*/
}
.test9:hover .box93 {
        animation: rotate 2s 2s linear;
        animation-fill-mode: forwards; /*保持结束位置*/
        backface-visibility: hidden;
}
.test9:hover .box922 {
        animation: rotate2 2s linear;
        animation-fill-mode: forwards; /*保持结束位置*/
}
.test9:hover .box92 {
        animation: rotate 2s linear;
        animation-fill-mode: forwards; /*保持结束位置*/
        backface-visibility: hidden;
}
.box92,
.box93,
.box94 {
        transform-origin: left center;
        left: 130px;
        border: 1px solid #000;
        width: 100px;
        height: 120px;
        z-index: 50;
        transform: rotateX(30deg) rotateY(0);
}
.box922,
.box933,
.box944 {
        left: 30px;
        border: 1px solid #000;
        width: 100px;
        height: 120px;
        transform-origin: right;
        transform:rotateX(30deg) rotateY(180deg);
}
.box91{
        left: 30px;
        border: 1px solid #000;
        width: 100px;
        height: 120px;
        transform: rotateX(30deg) rotateY(0);
}
.test9 div {
        position: absolute;
        transition: 2s;
        background-color: #fff;
        line-height: 110px;
        text-align: center;
}
.test9 {
        transform-style: preserve-3d;
        perspective: 1000px;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        // border: 1px solid #000;
        margin: 50px 50px;
        width: 250px;
        height: 120px;
}
@keyframes move {
        0% {
                background-position: 0px;
        }
        100% {
                background-position: 300px;
        }
}
.test81 {
        animation: move 3s infinite linear;
        border: 1px solid #000;
        background-size: 60px;
        background-image: linear-gradient(
                to right,
                #ffffff 25%,
                #48ff42 25%,
                #48ff42 50%,
                #ffffff 50%,
                #ffffff 75%,
                #48ff42 75%
        );
        width: 200px;
        height: 20px;
}
.test8 {
        margin-left: 30px;
        margin-top: 50px;
        height: 50px;
}
.test71 ul li:nth-child(1) {
        transform: rotateY(60deg) translateZ(250px);
}
.test71 ul li:nth-child(2) {
        transform: rotateY(120deg) translateZ(250px);
}
.test71 ul li:nth-child(3) {
        transform: rotateY(180deg) translateZ(250px);
}
.test71 ul li:nth-child(4) {
        transform: rotateY(240deg) translateZ(250px);
}
.test71 ul li:nth-child(5) {
        transform: rotateY(300deg) translateZ(250px);
}
.test71 ul li:nth-child(6) {
        transform: rotateY(360deg) translateZ(250px);
}
.test71 ul li {
        position: absolute;
}
.test71 ul {
        transition: 2s;
        transform-style: preserve-3d;
        position: relative;
        margin: 90px 210px;
}
.test71 img {
        width: 180px;
        height: 120px;
}
.test71:hover ul {
        transform: rotateY(360deg);
}
.test71 {
        perspective: 1000px;
        border: 1px solid #000;
        width: 600px;
        height: 300px;
}
.test7 {
        margin: auto 30px;
        margin-top: 50px;
        height: 300px;
}
.test62 {
        transform: rotateZ(45deg);
}
.test61 div:nth-of-type(1),
.test62 div:nth-of-type(1) {
        animation: loading 1.5s 0.25s infinite linear;
        left: 0;
        top: 0;
}
.test61 div:nth-of-type(2),
.test62 div:nth-of-type(2) {
        animation: loading 1.5s 0.5s infinite linear;
        top: 0;
        right: 0;
}
.test61 div:nth-of-type(3),
.test62 div:nth-of-type(3) {
        animation: loading 1.5s 0.75s infinite linear;
        bottom: 0;
        right: 0;
}
.test61 div:nth-of-type(4),
.test62 div:nth-of-type(4) {
        animation: loading 1.5s infinite linear;
        bottom: 0;
        left: 0;
}
.test6 .test61 div,
.test6 .test62 div {
        // animation: loading 1.5s infinite linear;
        position: absolute;
        background-color: rgb(106, 196, 238);
        width: 16px;
        height: 16px;
        border-radius: 50px;
}
@keyframes loading {
        0% {
                transform: scale(1);
        }
        50% {
                transform: scale(0);
        }
        100% {
                transform: scale(1);
        }
}
.test61,
.test62 {
        width: 60px;
        height: 60px;
        display: flex;
        justify-content: center;
        align-items: center;
        position: absolute;
}
.test6 {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 60px;
        height: 60px;
        position: relative;
        margin-top: 50px;
        margin-left: 50px;
}
@media screen and (max-width: 500px) {
        .test3 img {
                transition: 2s;
                width: 300px;
                height: 180px;
        }
}
.box2 {
        position: absolute;
        transform: perspective(1000px) translateY(-15px) rotateX(90deg);
}
.box1 {
        position: absolute;
        transform: perspective(1000px) translateZ(15px);
}
.test5:hover {
        transform: translateY(0px) rotateX(-90deg) translateZ(-0px);
        transition: 0.3s;
}
.test5 div {
        text-align: center;
        width: 60px;
        height: 30px;
        line-height: 30px;
        color: white;
        background-color: #000;
}
.test5 {
        display: inline-block;
        width: 60px;
        transform-style: preserve-3d;
        transition: 0.3s;
        position: relative;
        height: 30px;
}
.test55 {
        margin-left: 50px;
}
.plane6 {
        background-color: rgba(238, 49, 49, 0.5);
        transform: translateZ(-150px);
}
.plane5 {
        background-color: rgba(153, 49, 238, 0.5);
        transform: translateZ(150px);
}
.plane4 {
        background-color: rgba(90, 247, 0, 0.479);
        transform: translateX(150px) rotateY(-90deg);
}
.plane3 {
        background-color: rgba(4, 237, 253, 0.5);
        transform: translateX(-150px) rotateY(90deg);
}
.plane2 {
        background-color: rgba(57, 60, 245, 0.5);
        transform: translateY(150px) rotateX(-90deg);
}
.plane1 {
        background-color: rgba(238, 26, 203, 0.5);
        transform: translateY(-150px) rotateX(90deg);
}
.test4 div {
        position: absolute;
        width: 300px;
        height: 300px;
}
.test4:hover {
        transform: perspective(2500px) rotateY(-30deg) rotateX(30deg);
        transform-style: preserve-3d;
        transition: 1s;
}
.test4 {
        margin-top: 100px;
        transform: perspective(2500px) rotateY(30deg) rotateX(-30deg);
        transform-style: preserve-3d;
        margin-left: 100px;
        width: 500px;
        height: 500px;
        position: relative;
        font-size: 40px;
        text-align: center;
        line-height: 300px;
        transition: 1s;
}
.test3:hover img {
        transform: perspective(1500px) rotateY(30deg);
        transition: 1s;
}
.test3 {
        margin-bottom: 100px;
}
.test2:hover img {
        transform: scale(1.5) rotateZ(15deg);
        transition: 1s;
}
.test2:hover p:nth-of-type(1),
.test2:hover p:nth-of-type(2) {
        transform: translateY(-250px);
        transition: 1s;
}
.test2:hover h2 {
        transform: translateY(-250px);
        transition: 1s 0.2s;
}
.test2 h2 {
        color: #fff;
        transform: translateY(0px);
        font-size: 28px;
        width: 500px;
        text-align: center;
}
.test2 p:nth-of-type(1),
.test2 p:nth-of-type(2) {
        color: #fff;
        transform: translateY(0px);
        font-size: 28px;
        width: 500px;
        text-align: center;
}
.test2 {
        width: 500px;
        height: 300px;
        overflow: hidden;
}
input[type="checkbox"]::after {
        transition: 1s;
        content: "";
        display: block;
        width: 60px;
        height: 60px;
        position: absolute;
        left: -5px;
        top: -5px;
        border-radius: 30px;
        background: linear-gradient(to bottom, #d3d3d3, #9e9e9e);
        box-shadow: 0 2px 2px 0 #eee inset, 2px 1px 2px 0 #333;
}
input[type="checkbox"]:checked {
        background-color: #6fb500;
}
input[type="checkbox"]:checked::after {
        left: 75px;
}
input[type="checkbox"] {
        transition: 1s;
        -webkit-appearance: none;
        outline: none;
        margin: 50px;
        border: 10px solid #c1c1c1;
        border-radius: 50px;
        width: 150px;
        height: 70px;
        background-color: #888;
        position: relative;
        box-shadow: 0 0 10px 1px #3f3f3f inset;
}
.test {
        width: 100%;
        height: 100%;
        margin-bottom: 50px;
}
</style>