<template>
    <div>
        <div class='test' v-my-directive='message'  >
        </div>
        <div class='test' v-my-advance-directive='clickEvent'>
             {{message}}
        </div>
    </div>

</template>

<script>
    import myDirective from './my-directive';
    import myAdvanceDirective from './my-advance-directive';
	export default {
        directives: { myDirective , myAdvanceDirective},
		data() {
			return {
                message: 'hello'
			}
		},
		methods: {
            clickEvent() {
                this.message = Math.random() * 10 + 1;
            }
		},
		created:function() {

		}

	}
</script>
<style>
    * {
        padding:0;
        margin:0;
        box-sizing:border-box;
        font-family: Arial;
    }
    .test {
        width:100px;
        height:100px;
        background-color: steelblue;
        margin-bottom:10px;
    }
</style>