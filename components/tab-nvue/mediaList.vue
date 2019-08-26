<template>
<view>
    <view class="list-cell " style="padding:0px 20px  0px  20px;">

          <view class="media-list" v-if="options.title"   @click="bindClick" >

              <view style="display: flex;">
                  <view class="uni-list" style="flex: 6;">
                      <view class="uni-list-cell" >
                          <view class="uni-media-list">
                              <view class="uni-media-list-logo">
                                  <image :src="options.image_url"></image>
                              </view>
                              <view class="uni-media-list-body">
                                  <view class="uni-media-list-text-top">{{options.title}}</view>
                                  <view class="uni-text" style="display:flex;width: 100%;">
                                      <uni-rate :size="16" :disabled="true" :value="4" color="#bbb" active-color="#ffad00" @change="onChange" style="flex:1" /> <text class="uni-h5" style="flex:2;padding-left:0px;">4.9分</text></view>
                                  <view class="uni-h5" style="display:flex;width: 100%;"> 8个评价 <text class="uni-h5" style="flex:2;padding-left:0px;">查看</text></view>
                                  <view class="uni-media-list-text-bottom uni-ellipsis">业务范围:{{options.about}}</view>
                                  <view class="button-sp-area uni-h5" style="padding: 10px 0 0 0;">
                                      <button class="mini-btn" type="default" size="mini">预约</button>
                                      <button class="mini-btn"  type="primary"  size="mini" style="margin-left:10px;" hover-class="uni-list-cell-hover">下单</button>
                                  </view>
                              </view>
                          </view>
                      </view>
                  </view>
              </view>

          </view>

              <view class="media-list" v-if="options.title"   @click="bindClick" >

                  <view style="display: flex;">
                      <view class="uni-list" style="flex: 6;">
                          <view class="uni-list-cell" >
                              <view class="uni-media-list">
                                  <view class="uni-media-list-logo">
                                      <image :src="options.image_url"></image>
                                  </view>
                                  <view class="uni-media-list-body">
                                      <view class="uni-media-list-text-top">{{options.title}}</view>
                                      <view class="uni-text" style="display:flex;width: 100%;">
                                          <uni-rate :size="16" :disabled="true" :value="4" color="#bbb" active-color="#ffad00" @change="onChange" style="flex:1" /> <text class="uni-h5" style="flex:2;padding-left:0px;">4.9分</text></view>
                                      <view class="uni-h5" style="display:flex;width: 100%;"> 8个评价 <text class="uni-h5" style="flex:2;padding-left:0px;">查看</text></view>
                                      <view class="uni-media-list-text-bottom uni-ellipsis">业务范围:{{options.about}}</view>
                                      <view class="button-sp-area uni-h5" style="padding: 10px 0 0 0;">
                                          <button class="mini-btn" type="default" size="mini">预约</button>
                                          <button class="mini-btn"  type="primary"  size="mini" style="margin-left:10px;" hover-class="uni-list-cell-hover">下单</button>
                                      </view>
                                  </view>
                              </view>
                          </view>
                      </view>
                  </view>

              </view>

                  <view class="media-list" v-if="options.title"   @click="bindClick" >

                      <view style="display: flex;">
                          <view class="uni-list" style="flex: 6;">
                              <view class="uni-list-cell" >
                                  <view class="uni-media-list">
                                      <view class="uni-media-list-logo">
                                          <image :src="options.image_url"></image>
                                      </view>
                                      <view class="uni-media-list-body">
                                          <view class="uni-media-list-text-top">{{options.title}}</view>
                                          <view class="uni-text" style="display:flex;width: 100%;">
                                              <uni-rate :size="16" :disabled="true" :value="4" color="#bbb" active-color="#ffad00" @change="onChange" style="flex:1" /> <text class="uni-h5" style="flex:2;padding-left:0px;">4.9分</text></view>
                                          <view class="uni-h5" style="display:flex;width: 100%;"> 8个评价 <text class="uni-h5" style="flex:2;padding-left:0px;">查看</text></view>
                                          <view class="uni-media-list-text-bottom uni-ellipsis">业务范围:{{options.about}}</view>
                                          <view class="button-sp-area uni-h5" style="padding: 10px 0 0 0;">
                                              <button class="mini-btn" type="default" size="mini">预约</button>
                                              <button class="mini-btn"  type="primary"  size="mini" style="margin-left:10px;" hover-class="uni-list-cell-hover">下单</button>
                                          </view>
                                      </view>
                                  </view>
                              </view>
                          </view>
                      </view>

                  </view>
                      <view class="media-list" v-if="options.title"   @click="bindClick" >

                          <view style="display: flex;">
                              <view class="uni-list" style="flex: 6;">
                                  <view class="uni-list-cell" >
                                      <view class="uni-media-list">
                                          <view class="uni-media-list-logo">
                                              <image :src="options.image_url"></image>
                                          </view>
                                          <view class="uni-media-list-body">
                                              <view class="uni-media-list-text-top">{{options.title}}</view>
                                              <view class="uni-text" style="display:flex;width: 100%;">
                                                  <uni-rate :size="16" :disabled="true" :value="4" color="#bbb" active-color="#ffad00" @change="onChange" style="flex:1" /> <text class="uni-h5" style="flex:2;padding-left:0px;">4.9分</text></view>
                                              <view class="uni-h5" style="display:flex;width: 100%;"> 8个评价 <text class="uni-h5" style="flex:2;padding-left:0px;">查看</text></view>
                                              <view class="uni-media-list-text-bottom uni-ellipsis">业务范围:{{options.about}}</view>
                                              <view class="button-sp-area uni-h5" style="padding: 10px 0 0 0;">
                                                  <button class="mini-btn" type="default" size="mini">预约</button>
                                                  <button class="mini-btn"  type="primary"  size="mini" style="margin-left:10px;" hover-class="uni-list-cell-hover">下单</button>
                                              </view>
                                          </view>
                                      </view>
                                  </view>
                              </view>
                          </view>

                      </view>
    </view>
</view>
</template>

<script>
import uniRate from '@/components/uni-rate/uni-rate.vue'
export default {
    components: {
        uniRate
    },
    props: {
        options: {
            type: Object,
            default: function(e) {
                return {}
            }
        }
    },
    methods: {
        close(e) {
            this.$emit('close');
        },
        bindClick() {
            this.$emit('click');
        }
    }
}
</script>

<style>
.title {
    padding: 20upx;
}
</style>
