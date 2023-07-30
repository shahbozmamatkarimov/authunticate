<template>
  <header>
    <nav
      class="bg-blue-600 shadow fixed top-0 left-0 right-0 z-50 backdrop-blur-md w-full px-5 lg:px-20 py-2.5"
    >
      <div
        class="container py-1 overflow-hidden flex flex-wrap gap-10 w-full items-center mx-auto"
      >
        <img class="h-9 object-cover" src="../assets/svg/logo.svg" alt="logo" />
        <span class="h-8 w-1 bg-white"></span>
        <router-link class="font-bold text-xl text-white" to="/#"
          >Support Inbox</router-link
        >
      </div>
    </nav>
    <main>
      <section
        class="relative top-16 flex justify-center items-center md:h-[20rem] h-[40rem] text-white w-full"
      >
        <div class="absolute w-full md:h-[20rem] h-[40rem]">
          <img
            class="w-full h-full object-cover"
            src="../assets/bgImage.jpg"
            alt=""
          />
        </div>
        <div class="text-center z-10">
          <h1 class="md:text-2xl text-xl pb-5">Meta Business Help Center</h1>
          <p class="md:text-5xl text-3xl">Get Support</p>
        </div>
      </section>
      <section class="flex flex-col my-20 justify-center w-full pt-20 max-w-4xl mx-auto">
        <div class="mx-auto border-2 rounded-md overflow-hidden">
          <div class="flex bg-white gap-10 items-center p-5 border-b-2">
            <p class="rounded-full min-w-[3.5rem] h-14 w-14 bg-black"></p>
            <div>
              <h1 class="font-bold text-lg">
                Your page goes against our Community Standards
              </h1>
              <p class="text-gray-500">
                <button class="bg-blue-600 text-white px-2 py-1 rounded-md">
                  OPEN
                </button>
                CASE #2987491002757
              </p>
            </div>
          </div>
          <div class="text-gray-600 p-5">
            <h1 class="pb-5">ACTIVITY</h1>
            <div class="flex gap-10">
              <img
                class="h-14 w-14"
                src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Facebook_icon.svg/2048px-Facebook_icon.svg.png"
                alt=""
              />
              <div>
                <h1 class="font-bold text-black pt-2 pb-4">Our Message</h1>
                <p>
                  Your page has been scheduled for deletion because one of the
                  following resons:
                </p>
                <ul>
                  <li>- Intellectual Property Infingement</li>
                  <li>- Community Standards</li>
                  <li>- Hate Speech</li>
                </ul>
              </div>
            </div>
          </div>
          <hr class="border border-gray-300">
          <div>
            <div class="flex leading-[3rem] gap-10 p-5">
              <img
                class="h-14 w-14 object-cover"
                src="https://img.freepik.com/free-icon/user_318-563642.jpg?w=360"
                alt="img"
              />
              <div>
                <h1 class="font-bold text-2xl">Your Reply</h1>
                <p class="leading-6 pb-3 sm:text-md text-sm">
                  Please be sure to provide the requested information below. Failure to provide this information may delay the processing yout appeal.
                </p>
                <form class="flex flex-col">
                  <label for="name">Your name</label>
                  <input
                    class="border-2 border-gray-300 rounded-md"
                    id="name"
                    type="text"
                    required
                  />
                  <label for="tel">Your Phone Number</label>
                  <input
                    class="border-2 border-gray-300 rounded-md"
                    id="tel"
                    type="tel"
                    required
                  />
                  <label for="email">Login Email Address</label>
                  <input
                    class="border-2 border-gray-300 rounded-md"
                    id="email"
                    type="email"
                    required
                  />
                  <label for="textarea">Your Appeal</label>
                  <textarea
                    class="border-2 border-gray-300 rounded-md"
                    id="textarea"
                    rows="3"
                    required
                  ></textarea>
                  <div class="flex items-center gap-2">
                    <input
                      class="border-2 border-gray-300 rounded"
                      type="checkbox"
                      id="check"
                      required
                    />
                    <label for="check" class="font-medium leading-5 py-5">
                      Do you agree to our Terms. Data Policy and Cookies Policy.
                    </label>
                  </div>
                  <button class="bg-blue-600 rounded-md max-w-fit px-10 text-white font-bold" type="submit">
                    Submit
                  </button>
                </form>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </header>
</template>

<script setup></script>
