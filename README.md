# oasiisinfobytetask4
# akanksha vijay waman
<style>
    * {
        margin: 0;
        padding: 0;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
    }
      
    .container {
        width: 100%;
        height: 100vh;
        background-image: 
          linear-gradient(rgb(3, 73, 87), rgb(20, 121, 141));
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        
    }
      
    .container h1 {
        color: rgb(255, 255, 255);
        font-weight: 700;
        font-size: 25px;
        text-align: center;
    }
      
    .converter-row {
        display: flex;
        width: 50%;
        justify-content: space-between;
        align-items: center;
        background: rgb(0, 34, 56);
        border-radius: 10px;
        padding: 50px 20px;
    }
      
    .col {
        flex-basis: 32%;
        text-align: center;
    }
      
    .col label {
        font-size: 15px;
        font-weight: 500;
        margin-bottom: 10px;
        color: #fff;
    }
      
    .col input {
        width: 150px;
        height: 30px;
        background: white;
        border-radius: 5px;
        text-align: center;
    }
</style>
  
<div class="container">
    <h1> Temperature Converter</h1><br>
    <div class="converter-row">
        <div class="col">
            <label>Fahrenheit</label>
            <input type="number" id="fahrenheit">
        </div>
  
        <div class="col">
            <label>Celsius</label>
            <input type="number" id="celsius">
        </div>
  
        <div class="col">
            <label>Kelvin</label>
            <input type="number" id="kelvin">
        </div>
    </div>
</div>
  
<script>
    let celsius = document.getElementById('celsius');
    let fahrenheit = document.getElementById('fahrenheit');
    let kelvin = document.getElementById('kelvin');
    celsius.oninput = function () {
        let f = (parseFloat(celsius.value) * 9) / 5 + 32;
        fahrenheit.value = parseFloat(f.toFixed(2));
      
        let k = (parseFloat(celsius.value) + 273.15);
        kelvin.value = parseFloat(k.toFixed(2));
    }
    fahrenheit.oninput = function () {
        let c = ((parseFloat(
            fahrenheit.value) - 32) * 5) / 9;
        celsius.value = parseFloat(c.toFixed(2));
      
        let k = (parseFloat(
            fahrenheit.value) - 32) * 5 / 9 + 273.15;
        kelvin.value = parseFloat(k.toFixed(2));
    }
    kelvin.oninput = function () {
        let f = (parseFloat(
            kelvin.value) - 273.15) * 9 / 5 + 32;
        fahrenheit.value = parseFloat(f.toFixed(2));
      
        let c = (parseFloat(kelvin.value) - 273.15);
        celsius.value = parseFloat(c.toFixed(2));
    }
</script>
