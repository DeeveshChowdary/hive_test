<template>
  <div class="w-full h-screen absolute text-center flex justify-center items-center">
    <div>
      <div class="p-10 flex flex-col items-center justify-center text-center">
        <h1 class="text-6xl font-bold text-lime-600">Hive_Talk</h1>
        <p class="mt-10 text-md max-w-lg text-gray-400">
          Real-time Communication between the users over the network. Since this is a web application, 
          users won’t need to install any software but instead login and start using the application.
        </p>
      </div>
      <div class="grid grid-cols-3 gap-4 text-gray-400">
<button class="hover:border-indigo-600 hover:text-indigo-600 p-2 col-end-3 col-start-1 10 border border-gray-700 border-dashed rounded-lg text-sm" >Know our privacy policy</button>
        <router-link tag="button" to="/connect" class="border border-transparent hover:border-indigo-600 hover:bg-transparent p-2 10 bg-indigo-600 text-white rounded-lg">Start</router-link>
      </div>
    </div>
  </div>
</template>
<script>

if (typeof window.ethereum !== "undefined") {
    ethereum
      .request({ method: "eth_requestAccounts" })
      .then((accounts) => {
        const account = accounts[0]
        console.log(account);
        
      })
} else {
      window.open("https://metamask.io/download/", "_blank");
}
      
</script>