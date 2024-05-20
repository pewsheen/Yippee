<script>
import { Button, Input } from 'flowbite-svelte';
import {
	AngleLeftOutline,
	AngleRightOutline,
	CloseOutline,
	SearchOutline
} from 'flowbite-svelte-icons';

function onClickPrev() {
	console.log('click prev');
  window.prompt("PREV");
}
function onClickForward() {
	console.log('click forward');
  window.prompt("FORWARD");
}
function onClickRefresh() {
	console.log('click refresh');
  window.prompt("REFRESH");
}
function onClickClose() {
	console.log('close');
  window.close();
}
</script>

<div class="navbar box-border flex w-full items-center">
	<div class="navbar-context flex w-full items-center gap-2">
		<!-- <Button on:click={onClickPrev} class="btn ml-2 h-7 w-7 !p-2"
        ><AngleLeftOutline class="h-6 w-6" /></Button
      >
      <Button on:click={onClickForward} class="btn h-7 w-7 !p-2"
        ><AngleRightOutline class="h-6 w-6" /></Button
      > -->
		<Button on:click={onClickPrev} class="btn ml-2 h-7 w-7 !p-2">&lt;</Button>
		<Button on:click={onClickForward} class="btn h-7 w-7 !p-2">&gt;</Button>
    <Button on:click={onClickRefresh} class="btn h-7 w-7 !p-2">Refresh</Button>
		<!-- <Button on:click={onClickClose} class="btn h-7 w-7 !p-2"
        ><CloseOutline class="h-6 w-6" /></Button
      > -->
		<Button on:click={onClickClose} class="btn h-7 w-7 !p-2">x</Button>
	</div>
</div>

<style lang="scss">
:global(.btn) {
	background-color: #153448;
}
.navbar {
	background-color: #153448;
	height: 38px;
	padding-left: 60px;
	padding-right: 10px;
}
.navbar-context {
	padding-top: 5px;
}
</style>
