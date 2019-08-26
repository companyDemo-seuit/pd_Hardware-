<template>
<view class="example ">

    <uni-nav-bar :fixed="false" color="#333333" background-color="#FFFFFF" right-icon="scan" @click-left="showCity" @click-right="scan">
        <block slot="left">
            <view class="city">
                <view>{{ city }}</view>
                <uni-icon type="arrowdown" color="#333333" size="22" />
            </view>
        </block>
        <view class="input-view">
            <uni-icon type="search" size="22" color="#666666" />
            <input confirm-type="search" class="input" type="text" placeholder="输入搜索关键词" @confirm="confirm" />
        </view>
    </uni-nav-bar>
    <view class="swbg" style="padding-top:20px;padding-bottom:40px;">
        <media-list :options=" newsitem" @close="close(index1,index2)">
        </media-list>

    </view>
</view>
</template>
<script>
import uniNavBar from '@/components/uni-nav-bar/uni-nav-bar.vue'
import uniIcon from '@/components/uni-icon/uni-icon.vue'
import mediaList from '@/components/tab-nvue/mediaList.vue';
export default {
    components: {
        uniNavBar,
        uniIcon,
        mediaList
    },
    data() {
        return {
            city: '北京',
            newsitem: {
                "image_url": "https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/shuijiao.jpg?imageView2/3/w/200/h/100/q/90",
                "datetime": "40分钟前",
                "distance": 0,
                "title": "万达五金",
                "about": "封阳台、纱窗、移门、封阳台、纱窗、移门、封阳台、纱窗、移门",
                "star": 4,
                "rate": "4.9分",
                "comment_count": 0
            },
        }
    },
    onLoad(e) {
        this.title = e.title || '';
        this.test_get()
    },
    methods: {
        goDetail(e) {
            uni.navigateTo({
                url: '/pages/tabBar/dashboard/orderDetail/orderDetail?title=' + e.title
            });
        },
        showCity() {
          uni.showToast({
            title: '选择城市'
          });
        },
        scan() {
          uni.showToast({
            title: '扫码'
          });
        },

        test_get() {
          this.$request({
              url: '/admin/get_product_list',
              data: {
                a: 1
              }
            }, 'GET')
            .then(res => {
              // this.city = res
              console.log(res);
            });
        },
        test_post() {
          // 基本同GET
          this.$request({
    				url: '/admin/get_product_list'
    			}, 'POST')
            .then(res => {
              console.log(res);
            });
        }

    }
}
</script>
<style>
/* page {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    background:linear-gradient(top,rgb(49, 147, 186,1) 1%,rgb(117, 216, 250) 99%);
    background-size:100%
} */



/* 搜索框 */
.city {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    width: 100%;
    margin-left: 8px;
    white-space: nowrap;
}

.input-view {
    width: 92%;
    display: flex;
    background-color: #e7e7e7;
    height: 30px;
    border-radius: 15px;
    padding: 0 4%;
    flex-wrap: nowrap;
    margin: 7px 0;
    line-height: 30px;
}

.input-view .uni-icon {
    line-height: 30px !important;
}

.input-view .input {
    height: 30px;
    line-height: 30px;
    width: 94%;
    padding: 0 3%;
}

/* 搜索框 */
</style>
