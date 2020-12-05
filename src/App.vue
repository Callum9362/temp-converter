<template>
  <div id="app">
    <div class="container">
      <h1>Temperature Converter</h1>
      <div class="card">
        <div class="card-body">
          <div class="row">
            <div class="col-sm">
              <div class="row">
                <div class="col-sm">
                  <label for="degrees input">Degrees</label>
                </div>
              </div>
              <input type="text" class="form-control" placeholder="Degrees" aria-label="Username" aria-describedby="basic-addon1">
            </div>
            <div class="col-sm">
              <div class="row">
                <div class="col-sm">
                  <label for="type input">Type</label>
                </div>
              </div>
              <div class="input-group mb-3">
                <select class="custom-select" id="inputGroupSelect02">
                  <option selected>Choose...</option>
                  <option value="1">Celsius </option>
                  <option value="2">Fahrenheit</option>
                  <option value="3">Kelvin </option>
                </select>
              </div>
            </div>
            <div class="col-sm">
              <div class="row">
                <div class="col-sm">
                  <label for="pushing button down"></label>
                </div>
              </div>
                <button id="con-btn" type="button" class="btn btn-primary">Convert</button>
            </div>
          </div>
          <br>
          <div class="row">
            <div class="col-sm">
                <p>Your result</p>
                <p>22.222</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
