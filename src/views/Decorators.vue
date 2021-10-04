<template>
  <div>
   
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Decorators",
  mounted(){
      
function revert(...args: any){
    console.log(...args);
}

class User {
    a = "SimpleName";
    @revert
    b = this.a;
};

const newUser = new User();

console.log(":rocket: ~ file: test.js ~ line 26 ~ newUser", newUser.a);
console.log(":rocket: ~ file: test.js ~ line 28 ~ newUser", newUser.b);
  }
});
</script>