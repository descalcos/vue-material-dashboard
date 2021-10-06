<template>
  <div class="content">
    <div class="md-layout">
      <div class="md-layout-item">
        <md-card>
          <md-card-header data-background-color="blue">
            <h4 class="title">Notificações</h4>
            <p class="category">
              Feito à mão por nós com <i class="fa fa-heart heart"></i>
            </p>
          </md-card-header>
          <md-card-content>
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-100">
                <h5>Alertas</h5>
 
                <div data-background-color="red"
                  class="alert alert-info alert-with-icon"
                  data-notify="container"
                  >

                  <i data-notify="icon" class="material-icons">add_alert</i>
                  <span data-notify="message"
                    >Trocar Filtro</span
                  >
                </div>
                <div
                  class="alert alert-info alert-with-icon"
                  data-notify="container" div data-background-color="orange"
                >

                  <i data-notify="icon" class="material-icons">add_alert</i>
                  <span data-notify="message"
                    >Troca de Oleo marcado para o dia: 20/11/2021</span
                  >
                </div>
              </div>
              <div class="md-layout-item md-medium-size-100" >
                <h5>Boas Práticas</h5>
                <div class="alert alert-info " data-background-color="blue2">
                  <button type="button" aria-hidden="true" class="close">
                    ×
                  </button>
                  <span
                    >Não fique sempre com o combustivél na reversa</span
                  >
                </div>
                <div class="alert alert-success" data-background-color="blue">
                  <button type="button" aria-hidden="true" class="close">
                    ×
                  </button>
                  <span
                    >Assim que desligar o carro verifique todas luzes e aparelhos ligados</span
                  >
                </div>
                <div class="alert alert-warning" data-background-color="blue2">
                  <button type="button" aria-hidden="true" class="close">
                    ×
                  </button>
                  <span
                    >Av. BR32 a 10km, liguei os faróis!</span
                  >
                </div>
                <div class="alert alert-danger" data-background-color="blue">
                  <button type="button" aria-hidden="true" class="close">
                    ×
                  </button>
                  <span
                    >Coloque sem o cinto de segurança sempre</span
                  >
                </div>
                <div class="alert alert-primary" data-background-color="blue2">
                  <button type="button" aria-hidden="true" class="close">
                    ×
                  </button>
                  <span
                    >Verifique todos os retrovisores, se estão na posição correta</span
                  >
                </div>
              </div>

              
            </div>
          </md-card-content>
        </md-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      type: ["", "info", "success", "warning", "danger"],
      notifications: {
        topCenter: false
      }
    };
  },
  methods: {
    notifyVue(verticalAlign, horizontalAlign) {
      var color = Math.floor(Math.random() * 4 + 1);
      this.$notify({
        message:
          "Welcome to <b>Material Dashboard</b> - a beautiful freebie for every web developer.",
        icon: "add_alert",
        horizontalAlign: horizontalAlign,
        verticalAlign: verticalAlign,
        type: this.type[color]
      });
    }
  }
};
</script>
