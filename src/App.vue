<script setup>
import IconBrokenChain from "@/components/icons/IconBrokenChain.vue";
import IconInbox from "@/components/icons/IconInbox.vue";
</script>

<template>
  <div class="card-container">
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
.card-container {
  display: flex;
  gap: 20px;
}

.card {
  background-color: #fff;
  border-radius: 20px;
  width: 360px;
  overflow: hidden;
  padding: 10px;
  position: relative;
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

.card:hover {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  transition: all cubic-bezier(0.23, 1, 0.32, 1);
  padding: 10px;
}

.coming-soon {
  text-align: center;
  padding: 20px;
  background-color: #f9f9fb;
  border-radius: 16px;
}

.coming-soon__heading {
  font-size: medium;
  font-weight: 900;
  color: #1e1f24;
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
