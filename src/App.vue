<script setup>
import { ref } from 'vue'
import DomainModal from '@/components/Modal/DomainModal.vue'
import IconBrokenChain from "@/components/icons/IconBrokenChain.vue";
import IconInbox from "@/components/icons/IconInbox.vue";

const showModal = ref(false);


function closeModal(status) {
  showModal.value = status;

}
</script>

<template>
  <div class="card-container">
    <Teleport to="body">
      <DomainModal v-if="showModal" @close-modal="closeModal" />
      <button class="modal-button" @click="showModal = !showModal">Show Modal</button>
    </Teleport>
    <div class="card" v-for="card in 4" :key="card">
      <div class="inbox__icon">
        <div class="icon-container">
          <div class="icon">
            <IconInbox />
          </div>
        </div>


      </div>
      <div class="coming-soon">
        <IconBrokenChain />
        <p class="coming-soon__heading">Coming soon!</p>
        <p class="coming-soon__description">Stay tuned for future updates!</p>
      </div>
      <div class="card-content">

        <div class="card-headings">
          <h3 class="card-headings__heading">Inbox</h3>
          <span class="availability available">Available</span>
        </div>
        <p class="card-description">
          Manage support tickets, requests, and customer communication, all from one
          inbox.
        </p>
        <p class="category">Customer support software</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');

.card-container {
  display: flex;
  gap: 20px;

}

.modal-button {
  border-radius: 8px;
  border: 1px solid rgba(0, 7, 53, 0.15);
  padding: 8px;
  background-color: white;
  cursor: pointer;
  margin-top: 20px;

}

.card {
  background-color: #fff;
  border-radius: 20px;
  width: 360px;
  overflow: hidden;
  padding: 10px;
  position: relative;
}

.card:hover {
  border-radius: 20px;
  background: #FFF;
  box-shadow: 0px 10px 15px -3px rgba(0, 0, 0, 0.10), 0px 4px 6px 0px rgba(0, 0, 0, 0.05);
  padding: 10px;
}


.inbox__icon {
  position: absolute;
  top: 125px;
  left: 20px;
}


.icon-container {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  background-color: #eff0f3a6;
  display: flex;
  justify-content: center;
  align-items: center;
}

.icon {
  width: 38px;
  height: 38px;
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  border-radius: 999px;
  display: flex;
  justify-content: center;
  align-items: center;
}


.coming-soon {
  text-align: center;
  padding: 20px;
  background-color: #f9f9fb;
  border-radius: 16px;
}

.coming-soon__heading {
  color: #1E1F24;
  text-align: center;

  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 20px;
  margin-block-start: 20px;
  margin-block-end: 10px;
}

.coming-soon__description {
  color: #62636c;
  font-size: 14px;
  margin-block-start: 10px;
  margin-block-end: 10px;
}

.card-headings {
  display: flex;
  justify-content: space-between;
}

.card-headings__heading {
  color: #1e1f24;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: 24px;
}

.card-content {
  padding: 10px;
}

.availability {
  display: inline-block;
  padding: 4px 8px;
  border-radius: 4px;
  font-size: 12px;
}

.availability.available {
  background-color: rgba(2, 179, 2, 0.079);
  color: #006316;
  margin: auto 0;
  border-radius: 999px;
}

.card-description {
  color: #62636c;
  font-size: 14px;
  width: 244px;
  text-align: left;
  margin-block-start: 0px;
  margin-block-end: 0px;
}

.category {
  font-size: 12px;
  color: #1e1f24;
  margin-block-start: 10px;
  margin-block-end: 0px;
}
</style>
