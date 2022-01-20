<script>
    import {FeedbackStore} from '../../stores'
     let count
     let average

    $: count = $FeedbackStore.length
	$: average = Number.parseFloat($FeedbackStore.reduce((a,{rating})=>a+rating,0) / $FeedbackStore.length).toFixed(2)

</script>

<div class="feedback-stats">
    <h4>{count} Reviews</h4>
    <h4>Ratings average {average}</h4>
</div>

<style>
    .feedback-stats{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>