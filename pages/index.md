# Custom Components
<!-- You need to import the component. You can reference your components folder as '$lib' -->
<script>
    import Hello from '$lib/Hello.svelte';
    import Slider from '$lib/Slider_boolean.svelte';
    $: swapXY_switch = true;
</script>

```sql sales_by_country 
select 'Canada' as country, 100 as sales_usd, 'yellow' as color, 20 as income_usd
union all 
select 'USA' as country, 200 as sales_usd, 'blue' as color,  40 as income_usd
union all 
select 'UK' as country, 300 as sales_usd, 'red' as color, 60 as income_usd  
```

To use data in the component, pass it to the component as a prop
You can use multiple queries, and name the props anything you like

<Slider bind:value={swapXY_switch}/>

The swapXY is: **{swapXY_switch}**

<Hello 
  query={sales_by_country}
  bind:swapXY={swapXY_switch}
  y=sales_usd
/>