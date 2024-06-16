<template>
  <div class="uploadList">
    <van-uploader v-model="fileList" ref="uploadRef" class="box" :after-read="afterRead" accept="image/*"
      :max-size="10 * 1024 * 1024" :preview-full-image="false" :max-count="7"  multiple
      :full="true">

      
      <!-- 如果使用这张图片，上传5张后会消失，第四张上传后会变很小，如果不使用，原生上传图标会变很小-->
      <img src="./assets/添加图片.png"  style="display: inline-block; max-width: 100%; max-height: 100%">
      
      <template #preview-cover="{ file }">
        <div class="preview-cover van-ellipsis">点击编辑</div>
      </template>
    </van-uploader>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fileList:[]
    };
  },

  methods: {
    afterRead(){

    },

    
  },
};
</script>

<style lang="less">
.uploadList{
  width: 100%;
}

.van-uploader{
  width: 100%;
}

.van-uploader__wrapper{

  display: flex;
  flex-wrap: nowrap;
  overflow: scroll;
  width: 100%;
}
.preview-cover {
  position: absolute;
  bottom: 0;
  box-sizing: border-box;
  width: 100%;
  padding: 4px;
  color: #fff;
  font-size: 12px;
  text-align: center;
  background: rgba(0, 0, 0, 0.6);
}
</style>
