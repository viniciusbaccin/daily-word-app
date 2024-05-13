<template>
  <q-page class="flex flex-center bg-color">
    <div style="height: 90vh; width: 30%;">
      <div class="row q-pa-md flex flex-center">
        <q-btn round flat class="btn-color" text-color="white" icon="calendar_month" size="lg">
          <q-tooltip>
            <div>Calendário</div>
          </q-tooltip>
        </q-btn>
        <q-btn round flat class="btn-color q-mx-lg" text-color="white" icon="star" size="lg">
          <q-tooltip>
            <div>Favoritas</div>
          </q-tooltip>
        </q-btn>
        <q-btn round flat class="btn-color" text-color="white" icon="settings" size="lg">
          <q-tooltip>
            <div>Configurações</div>
          </q-tooltip>
        </q-btn>
      </div>
      <div class="q-px-lg" style="height: 50vh;">
        <div>
          <h4 class="q-pt-md" style="color: #1b2727; padding-top: 120px;">Paralelepipedo</h4>
        </div>
        <div>
          <span class="text-body1" style="color: #1b2727;">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quos blanditiis tenetur unde suscipit, quam beatae rerum inventore consectetur, neque doloribus, cupiditate numquam dignissimos laborum fugiat deleniti? Eum quasi quidem quibusdam.
          </span>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage'
})
</script>

<style>
.bg-color {
  background: rgb(178,197,178);
  background: linear-gradient(11deg, rgba(178,197,178,1) 0%, rgba(213,221,223,1) 100%);
}

.btn-color {
  background: rgb(27,39,39);
  background: linear-gradient(0deg, rgba(27,39,39,1) 0%, rgba(60,81,72,1) 100%);
}
</style>
