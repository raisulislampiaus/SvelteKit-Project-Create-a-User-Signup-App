<script>
    export let dateOfBirth = { day: '', month: '', year: '' };
  </script>
  
  <style>
    .dob-group {
      display: flex;
      justify-content: space-between;
    }
    select {
      width: calc(33% - 10px);
      padding: 8px;
      margin: 5px 0;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
  </style>
  
  <div class="dob-group">
    <select bind:value={dateOfBirth.day}>
      <option value="" disabled>Day</option>
      {#each Array(31).fill(0).map((_, i) => i + 1) as day}
        <option value={day}>{day}</option>
      {/each}
    </select>
    <select bind:value={dateOfBirth.month}>
      <option value="" disabled>Month</option>
      <option value="1">Jan</option>
      <option value="2">Feb</option>
      <option value="3">Mar</option>
      <option value="4">Apr</option>
      <option value="5">May</option>
      <option value="6">Jun</option>
      <option value="7">Jul</option>
      <option value="8">Aug</option>
      <option value="9">Sep</option>
      <option value="10">Oct</option>
      <option value="11">Nov</option>
      <option value="12">Dec</option>
    </select>
    <select bind:value={dateOfBirth.year}>
      <option value="" disabled>Year</option>
      {#each Array(new Date().getFullYear() - 1900).fill(0).map((_, i) => i + 1900) as year}
        <option value={year}>{year}</option>
      {/each}
    </select>
  </div>
  