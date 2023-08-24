<template>
  <div>
    <div class="p-1 d-inline-block">
      <strong>Tên:</strong>
      {{ contact.name }}
    </div>

    <div class="p-1 d-inline-block">
      <strong>E-mail:</strong>
      {{ contact.email }}
    </div>
    <div class="p-1 d-inline-block">
      <strong>Địa chỉ:</strong>
      {{ contact.address }}
    </div>
    <div class="p-1 d-inline-block">
      <strong>Điện thoại:</strong>
      {{ contact.phone }}
    </div>
    <div class="p-1 d-inline-block">
      <strong>Liên hệ yêu thích:&nbsp;</strong>
      <i v-if="contact.favorite" class="fa fa-check"></i>
      <i v-else class="fa fa-times"></i>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    contact: {
      type: Object,
      required: true,
    },
  },
};
</script>
