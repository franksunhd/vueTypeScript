<template>
    <div class="home">
        <h1>boolean:{{bool.toString()}}</h1>
        <h1>string:{{str.toString()}}</h1>
        <h1>number:{{num.toString()}}</h1>
        <button @click="clickBtn">点击</button>
    </div>
</template>

<script lang="ts">
	import {defineComponent, ref} from "vue";

	export default defineComponent({
		name: "HomeView",
		setup() {
			let bool = ref<boolean>(true);
			let str = ref("123");
			let num = ref<number>(12);

			function clickBtn() {
				num.value++;
			}

			return {bool, str, num, clickBtn};
		}

	});
</script>
