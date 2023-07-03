<template>
  <div>
    <div class="modal" :class="{ 'd-block': showModal }">
      <div class="modal-dialog">
        <div class="modal-content">
          <!-- 모달 내용 -->
          <div class="modal-header">
            <h5 class="modal-title">AI-Driven Detection</h5>
          </div>
          <div class="modal-body">
            <button type="button" class="btn btn-primary">Activate</button>
          </div>
        </div>
      </div>
    </div>
    <div
      class="modal-backdrop"
      :class="{ show: showModal }"
      @click="showModal = false"
    ></div>
  </div>
</template>

<script>
export default {
  name: "credit-card",
  data() {
    return {
      showModal: true,
    };
  },
};
</script>

<style>
.modal-backdrop {
  backdrop-filter: blur(5px);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  opacity: 0;
  transition: opacity 0.3s ease;
}
.modal-dialog{
  margin : 15rem auto !important;
}
.modal-body{
  display: flex;
  justify-content: center;
  align-items: center;
}
.modal-backdrop.show {
  opacity: 1;
}
</style>
