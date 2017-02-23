<template>
	<ul v-if="seller.supports" class="support">
		<li class="support-item border-1px" v-for="(item, index) in seller.supports">
			<span class="icon" :class="classMap[seller.supports[index].type]"></span>
		    <span class="text">{{seller.supports[index].description}}</span>
		</li>
	</ul>
</template>

<script type="text/ecmascript-6">
  const LENGTH = 5;
  const CLS_ON = 'on';
  const CLS_HALF = 'half';
  const CLS_OFF = 'off';
  
  export default {
    props: {
        seller: {
            type: Object
        }
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
    @import '../../common/stylus/mixin.styl';
</style>