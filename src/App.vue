<template>
  <div class="mx-auto w-full h-screen justify-center bg-[#F3F3F3]">
    <h1 class="text-center text-2xl text-black py-10">
      ~ ToDo List Application ~
    </h1>
    <div class="flex flex-col w-full max-w-sm mx-auto my-4">
      <div class="relative flex items-center w-full">
        <input
          v-model="newItem"
          class="w-full py-2 px-2 rounded text-slate-600"
          placeholder="Add Todo..." />
        <button
          class="absolute right-0 h-full px-4 py-2 rounded text-white bg-[#7999fd] cursor-pointer"
          @click="addNewItem">
          Add
        </button>
      </div>
      <div class="flex flex-col space-y-4">
        <div
          v-for="item in itemList"
          :key="item.id"
          class="flex items-center justify-between w-full bg-[#7999fd] rounded-lg px-4 py-2">
          <p class="text-white">{{ item.value }}</p>
          <button
            class="text-white rounded border border-white px-2 h-7 self-center cursor-pointer"
            @click="removeItem(item)">
            Remove
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  import { ref } from "vue";

  const itemList = ref([
    { id: 0, value: "Buy milk" },
    { id: 1, value: "Go for a run" },
    { id: 2, value: "Complete project" },
  ]);

  const newItem = ref("");

  function addNewItem() {
    if (newItem.value.trim() !== "") {
      itemList.value.push({ id: itemList.value.length, value: newItem.value });
      newItem.value = "";
    }
  }

  function removeItem(item) {
    itemList.value = itemList.value.filter((i) => i.id !== item.id);
  }
</script>

