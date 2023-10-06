<template>
  <div>
    <h3 class="p-3 text-center">Vue HTTP GET Requests with Fetch</h3>
    <get-request/>
    <get-request-async-await/>
    <get-request-error-handling/>
    <get-request-set-headers/>
  </div>
  <div>
    <h3 class="p-3 text-center">Counter test</h3>
    <hello-world/>
  </div>
  

</template>

<script>
import GetRequest from './components/GetRequest.vue'
import HelloWorld from './components/HelloWorld.vue'
import GetRequestAsyncAwait from './components/GetRequestAsyncAwait.vue'
import GetRequestErrorHandling from './components/GetRequestErrorHandling.vue'
import GetRequestSetHeaders from './components/GetRequestSetHeaders.vue'


export default {
  name: "app",
  components: {
    GetRequest,
    GetRequestAsyncAwait,
    GetRequestErrorHandling,
    GetRequestSetHeaders,
    HelloWorld,
  }
};
</script>
