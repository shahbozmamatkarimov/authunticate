<template>
  <main class="flex justify-center items-center min-h-screen">
    <section class="max-w-[40rem] rounded-md overflow-hidden border-2 bg-white">
      <h1 class="bg-gray-100 font-bold p-5">
        Two-factor authentication required
      </h1>
      <p class="py-3 px-5">
        You've asked us to require a 6-digit login code when anyone tries to
        access your account from a new device or browser.
      </p>
      <p class="py-3 px-5">
        Enter the 6-digit code from your code generator or third-party app
        below.
      </p>
      <form @submit.prevent="sendCode">
        <div class="py-3 px-5 pb-10 flex gap-10 items-center">
          <input v-model="code" class="rounded-md" type="text" placeholder="Login code" />
          <span id="timer"></span>
        </div>
        <div class="bg-gray-100 flex w-full justify-between items-center p-5">
          <p class="text-blue-800 font-bold">
            Need another way to authenticate?
          </p>
          <button class="py-2 px-5 bg-blue-600 rounded-md text-white font-bold">
            Send
          </button>
        </div>
      </form>
    </section>
  </main>
</template>

<script setup>
const code = ref("");
const sendCode = () => {
    code.value = "";
}

onMounted(() => {
  document.getElementById("timer").innerHTML = '05' + ":" + '00';
  startTimer();

  function startTimer() {
    var presentTime = document.getElementById("timer").innerHTML;
    var timeArray = presentTime.split(/[:]+/);
    var m = timeArray[0];
    var s = checkSecond(timeArray[1] - 1);
    if (s == 59) {
      m = m - 1;
    }
    if (m < 0) {
      return;
    }

    document.getElementById("timer").innerHTML = m + ":" + s;
    console.log(m);
    setTimeout(startTimer, 1000);
  }

  function checkSecond(sec) {
    if (sec < 10 && sec >= 0) {
      sec = "0" + sec;
    } // add zero in front of numbers < 10
    if (sec < 0) {
      sec = "59";
    }
    return sec;
  }
});
</script>

<style lang="scss" scoped>
div {
  font-size: 20px;
  text-align: center;
}
</style>
