<script setup>
  const liste = ["Achat", "Retrait", " Solde"];
</script>
<template>
  <div class="mx-44 w-[800px] h-[450px] justify-center bg-slate-400">
    <h1 class="text-center text-2xl text-white py-10">ToDo List Application</h1>
    <div class="flex w-[80%] rounded-md bg-white my-4 m-auto">
      <input
        class="flex flex-1 py-2 px-2 rounded text-slate-600"
        placeholder="Add Todo..." />
      <button
        class="flex flex-2 w-[80px] justify-center items-center text-white bg-slate-600 cursor-pointer">
        Add to list
      </button>
    </div>
    <div class="flex flex-col space-y-6">
      <div class="flex w-[80%] bg-slate-600 m-auto mt-4 justify-between">
        <p class="px-6 py-2 text-white">To Do Item</p>
        <button
          class="text-white border border-white px-2 h-7 mx-4 self-center cursor-pointer">
          remove
        </button>
      </div>
      <div class="flex w-[80%] bg-slate-600 m-auto justify-between">
        <p class="px-6 py-2 text-white">To Do Item</p>
        <button
          class="text-white border border-white px-2 h-7 mx-4 self-center cursor-pointer">
          remove
        </button>
      </div>
      <div class="flex w-[80%] bg-slate-600 m-auto justify-between">
        <p class="px-6 py-2 text-white">To Do Item</p>
        <button
          class="text-white border border-white px-2 h-7 self-center mx-4 cursor-pointer">
          remove
        </button>
      </div>
    </div>
  </div>
  <!-- <div class="flex w-[600px] bg-black">1234567</div> -->
</template>
<style>
  @import "./style.css";
</style>

