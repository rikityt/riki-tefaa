<template>
  <div>
    <canvas id="statistik"></canvas>
  </div>
  </template>
  
  <script setup>
  import Chart from 'chart.js/auto';
  
  const labels = [
    'january',
    'february',
    'march',
    'april',
    'mei',
    'june',
  ];
  const data ={
    labels:labels,
    datasets:[{
      label: 'pengunjung',
      data: [6, 8, 10, 9, 9,3],
      backgroundColor:[
        'rgb(43, 191, 254)',
        'rgb(255, 0, 0)',
        'rgb(124, 252, 2)',
        'rgb(0, 0, 0)',
        'rgb(249, 4, 147)',
        'rgb(0, 0, 205)'
      ],
    }]
  };
  const  config ={
    type: 'bar',
    data: data,
    options: {}
  };
  onMounted(()=>{
    const myChart = new Chart(
      document.getElementById('statistik'),
      config
    );
  })
  
</script>
