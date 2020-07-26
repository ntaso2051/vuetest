<template>
  <div>
    <p>Hello World !!</p>
    <button @click="sendGet">get</button>
    <button @click="sendPost">post</button>
    <button @click="sendPut">put</button>
    <button @click="sendDelete">delete</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Axios",
  methods: {
    sendGet() {
      axios.get("http://150.95.211.46:10300");
    },
    sendPost() {
      axios.post("http://150.95.211.46:10300", {
        traQID: "to-hutohu",
        grade: 16
      });
    },
    sendPut() {
      axios.put("http://150.95.211.46:10300", {
        testData: { string: "string", number: 1 }
      });
    },
    sendDelete() {
      axios.delete("http://150.95.211.46:10300", {
        data: { po: 1 }
      });
    }
  }
};
</script>
