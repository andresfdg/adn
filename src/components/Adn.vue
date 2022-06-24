<template>
  <div class="container">
    <form @submit.prevent="div()">
      <div class="mb-3">
        <label class="form-label" for="exampleFormControlInput"
          ><h5>Insert DNA</h5></label
        >
        <input
          type="text"
          id="exampleFormControlInput"
          placeholder="insert DNA"
          v-model="adn"
          class="form-control"
        />
      </div>

      <div class="mb-3">
        <label class="form-label" for="exampleFormControlInput1"
          ><h5>Insert RS</h5></label
        >
        <input
          type="text"
          id="exampleFormControlInput1"
          placeholder="insert SR"
          v-model="rs"
          class="form-control"
        />
      </div>

      <button class="btn btn-primary mt-3" type="submit">
        <i class="bx bxs-send"></i>
      </button>
    </form>

    <div class="robot">
      <span>
        <h1>{{ resultado }}</h1>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      adn: "",
      rs: "",
      resultado: "",
    };
  },

  methods: {
    div() {
      var ADN, RSL, SR, c, i, j;
      ADN = this.adn;
      SR = this.rs;

      RSL = SR.length;
      c = 0;
      i = 0;
      j = 0;

      for (
        var i, _pj_c = 0, _pj_a = ADN, _pj_b = _pj_a.length;
        _pj_c < _pj_b;
        _pj_c += 1
      ) {
        i = _pj_a[_pj_c];

        if (SR === ADN.slice(j, j + RSL)) {
          c = c + 1;
        }
        j = j + 1;
      }

      this.resultado = c;
      return this.resultado;
    },
  },
};
</script>

<style scoped>
.container {
  margin-top: 2rem;
}

.robot {
  margin-top: 2rem;
}
</style>
