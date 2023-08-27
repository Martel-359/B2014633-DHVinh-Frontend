<template>
  <div class="page">
    <h4>Thêm mới liên hệ</h4>
    <ContactFormAdd @submit:contact="createContact" />
  </div>
  <p>{{ message }}</p>
</template>

<script>
import ContactFormAdd from "@/components/ContactFormAdd.vue";
import ContactService from "@/services/contact.service.js";

export default {
  components: {
    ContactFormAdd,
  },
  props: {
    contact: { type: Object, require: true },
  },
  data() {
    return {
      message: "",
    };
  },
  methods: {
    async createContact(data) {
      try {
        await ContactService.create(data);
        this.message = "Thêm liên hệ thành công";
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>
