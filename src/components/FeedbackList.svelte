<script>
    import {FeedbackStore} from '../../stores'
    import {fade,scale} from 'svelte/transition'
    import FeedbackItem from './FeedbackItem.svelte'
    import { onMount,onDestroy } from 'svelte';
    // let feedback = []

    // const unsubscribe = FeedbackStore.subscribe((data)=>feedback = data)

    // onMount (()=>{
    //     console.log('mount');
    // })

    // onDestroy (()=>{
    //     unsubscribe()
    // })
    //console.log(feedback);
</script>

{#each $FeedbackStore as fb (fb.id)}
<div transition:fade>
    <!-- <div in:scale out:fade="{{duration:500}}"> -->
    <FeedbackItem item={fb}  />
</div>
{/each}