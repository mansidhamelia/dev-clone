<template>
  <div class="flex flex-row m-auto px-6 justify-between">
    <div class="flex-none h-14 w-14 relative">
      <img
        src="../assets/logo.png"
        alt=""
        @click="goTo"
        class="absolute inset-0 w-full h-full object-cover rounded-t-3xl"
      />
    </div>
    <div class="flex flex-row justify-items-start gap-2">
      <button
        class="
          p-2
          h-10
          w-44
          text-xl
          font-bold
          flex
          items-center
          justify-center
          hover:shadow-lg hover:border-transparent
          shadow-md
          rounded-lg
          bg-gradient-to-r
          hover:from-gray-200
          active:shadow-inner
        "
        @click="newData"
      >
        NEW
      </button>
      <button
        class="
          p-2
          h-10
          w-4/5
          font-bold
          text-xl
          flex
          items-center
          justify-center
          hover:shadow-lg hover:border-transparent
          shadow-md
          rounded-lg
          bg-gradient-to-r
          hover:from-gray-200
          active:bg-red-200
        "
        @click="top"
      >
        TOP
      </button>
    </div>
  </div>
</template>


<script>
export default {
  methods: {
    goTo() {
      this.$router.push("/articles").catch(() => {});
    },
    top() {
      this.$router.push("/articles/top").catch(() => {});
    },
    newData() {
      this.$router.push("/articles/new").catch(() => {});
    },
  },
};
</script>