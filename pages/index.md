# Custom Components
<!-- You need to import the component. You can reference your components folder as '$lib' -->
<script>
    import Hello from '$lib/Hello.svelte';
    import Slider from '$lib/Slider_boolean.svelte';
    $: year = 2000;
</script>

```sql sales_by_country 
select 'Canada' as country, 100 as sales_usd, 'yellow' as color, 20 as income_usd, 2000 as year union all 
select 'Canada' as country, 120 as sales_usd, 'yellow' as color, 30 as income_usd, 2001 as year union all 
select 'Canada' as country, 150 as sales_usd, 'yellow' as color, 40 as income_usd, 2002 as year union all 
select 'Canada' as country, 160 as sales_usd, 'yellow' as color, 50 as income_usd, 2003 as year union all 
select 'Canada' as country, 180 as sales_usd, 'yellow' as color, 60 as income_usd, 2004 as year union all 
select 'USA' as country, 200 as sales_usd, 'yellow' as color, 25 as income_usd, 2000 as year union all 
select 'USA' as country, 300 as sales_usd, 'yellow' as color, 35 as income_usd, 2001 as year union all 
select 'USA' as country, 400 as sales_usd, 'yellow' as color, 45 as income_usd, 2002 as year union all 
select 'USA' as country, 500 as sales_usd, 'yellow' as color, 55 as income_usd, 2003 as year union all 
select 'USA' as country, 600 as sales_usd, 'yellow' as color, 65 as income_usd, 2004 as year union all 
select 'UK' as country, 270 as sales_usd, 'yellow' as color, 20 as income_usd, 2000 as year union all 
select 'UK' as country, 370 as sales_usd, 'yellow' as color, 30 as income_usd, 2001 as year union all 
select 'UK' as country, 470 as sales_usd, 'yellow' as color, 40 as income_usd, 2002 as year union all 
select 'UK' as country, 570 as sales_usd, 'yellow' as color, 50 as income_usd, 2003 as year union all 
select 'UK' as country, 670 as sales_usd, 'yellow' as color, 60 as income_usd, 2004 as year
```

To use data in the component, pass it to the component as a prop
You can use multiple queries, and name the props anything you like

<Slider bind:value={year}/>

The year is: **{year}**

<Hello 
  query={sales_by_country.filter(d=>d.year===year)}
  bind:swapXY={year}
  y=sales_usd
/>