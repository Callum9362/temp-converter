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
              <input
                type="number"
                class="form-control"
                placeholder="Degrees"
                aria-label="Username"
                aria-describedby="basic-addon1"
                v-model="fromValue"
                required
              />
            </div>
            <div class="col-sm">
              <div class="row">
                <div class="col-sm">
                  <label for="type input">Type</label>
                </div>
              </div>
              <div class="input-group mb-3">
                <select
                  v-model="option"
                  class="custom-select"
                  id="inputGroupSelect"
                >
                  <option selected>Choose...</option>
                  <option value="1">{{ units[0] }}</option>
                  <option value="2">{{ units[1] }}</option>
                </select>
              </div>
            </div>
            <div class="col-sm">
              <div class="row">
                <div class="col-sm">
                  <label for="pushing button down"></label>
                </div>
              </div>
              <button
                @click="convert(fromValue, option, result)"
                id="con-btn"
                type="button"
                class="btn btn-primary"
              >
                Convert
              </button>
            </div>
          </div>
          <br />
          <div class="row">
            <div class="col-sm">
              <p>The answer is...</p>
              <p>{{ result }}</p>
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
  data() {
    return {
      fromValue: 0,
      units: ["Fahrenheit", "Kelvin"],
      result: 0,
      option: 0,
    };
  },
  methods: {
    convert: function (fromValue, option, result) {
      if (option == 1) {
        console.log("Fahrenheit was chosen");
        result = (fromValue * 1.8) + 32;
        console.log("The result was " + result);
        return result;
      }

      if (option == 2) {
        console.log("Kelvin was chosen");
        result = fromValue + 273.15;
        console.log("The result was " + result);
        return result;
      } else {
        console.log("There has been an error with your input please review.");
        console.log(fromValue);
        console.log(option);
        return fromValue;
      }
    },
  },
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
