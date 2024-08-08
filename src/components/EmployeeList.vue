<template>
    <div class="employee-container">
      <h2 class="employee-title">Listes Des Employés</h2>
      <ol class="employee-list">
        <li v-for="(employee, index) in employees" :key="index" @mouseover="hover = index" @mouseleave="hover = null" :class="{ hover: hover === index }">
          {{ employee.name }}
        </li>
      </ol>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        employees: [
          { name: 'Fatouma Cisse' },
          { name: 'Mohamed Bankolé' },
          { name: 'Ndiaye Camara' },
        ],
        hover: null
      };
    }
  };
  </script>
  
  <style scoped>
  .employee-container {
    text-align: center;
    margin: 20px auto;
    max-width: 400px;
    padding: 10px;
    background-color: #f0f8ff;
    border: 2px solid #00008b;
    border-radius: 10px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .employee-title {
    font-size: 24px;
    color: #00008b;
    margin-bottom: 15px;
    font-family: 'Arial', sans-serif;
    text-transform: uppercase;
    letter-spacing: 2px;
  }
  
  .employee-list {
    list-style-type: decimal;
    padding: 0;
    margin: 0;
  }
  
  .employee-list li {
    padding: 15px;
    background-color: #87cefa;
    margin: 5px;
    border-radius: 5px;
    color: #00008b;
    font-weight: bold;
    font-family: 'Arial', sans-serif;
    transition: background-color 0.3s ease, color 0.3s ease;
  }
  
  .employee-list li.hover {
    background-color: #ffd700;
    color: #ffffff;
  }
  
  .employee-list li:not(.hover):hover {
    background-color: #1e90ff;
    color: #ffffff;
  }
  </style>
  