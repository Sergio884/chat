<template>
  <div class="row q-px-md">
    <div class="col">
      <span
        class="text-weight-bolder"
        style="font-size: 12px"
        v-text="'Wallet'"
      ></span>
      <q-separator
        color="orange"
        style="height: 1px; width: 30px; margin-top: -2px"
      />
    </div>
  </div>

  <div class="row full-width">
    <q-card
      bordered
      style="border-color: #9451db"
      class="border-rounded col q-ma-md"
    >
      <q-card-section>
        <div class="row">
          <div class="col-sm-3 q-mr-xs">
            <q-avatar color="purple">
              <q-icon name="las la-wallet" color="white" />
            </q-avatar>
          </div>
          <div class="col">
            <div
              class="text-weight-medium"
              style="font-size: 12px"
              v-text="'Saldo General:'"
            />
            <div
              style="font-size: 20px"
              class="text-left text-weight-bold"
              v-text="'$106,970.10'"
            ></div>
          </div>
        </div>
      </q-card-section>
    </q-card>

    <q-card
      bordered
      style="border-color: #9451db"
      class="border-rounded col q-ma-md"
    >
      <q-card-section>
        <div class="row">
          <div class="col-sm-3 q-mr-xs">
            <q-avatar color="purple">
              <q-icon name="las la-wallet" color="white" />
            </q-avatar>
          </div>
          <div class="col">
            <div
              class="text-weight-medium"
              style="font-size: 12px"
              v-text="'Saldo General:'"
            />
            <div
              style="font-size: 20px"
              class="text-left text-weight-bold"
              v-text="'$106,970.10'"
            ></div>
          </div>
        </div>
      </q-card-section>
    </q-card>

    <q-card
      bordered
      style="border-color: #9451db"
      class="border-rounded col q-ma-md"
    >
      <q-card-section>
        <div class="row">
          <div class="col-sm-3 q-mr-xs">
            <q-avatar color="purple">
              <q-icon name="las la-wallet" color="white" />
            </q-avatar>
          </div>
          <div class="col">
            <div
              class="text-weight-medium"
              style="font-size: 12px"
              v-text="'Saldo General:'"
            />
            <div
              style="font-size: 20px"
              class="text-left text-weight-bold"
              v-text="'$106,970.10'"
            ></div>
          </div>
        </div>
      </q-card-section>
    </q-card>
  </div>

  <div class="row q-px-md">
    <div class="col">
      <span
        class="text-weight-bolder"
        style="font-size: 12px"
        v-text="'Transacciones'"
      ></span>
      <q-separator
        color="orange"
        style="height: 1px; width: 65px; margin-top: -2px"
      />
    </div>
  </div>

  <div class="horizontal-center row q-pa-md">
    <q-card flat bordered class="full-width border-rounded row">
      <div class="col-xs-12 col-sm-2">
        <div v-text="'Transacción'"></div>
        <div v-text="'#123'"></div>
      </div>
      <div class="col-xs-12 col-sm-6 row">
        <span>Tipo</span>
      </div>
      <div class="col">
        <span>Concepto</span>
      </div>
      <div class="col">Tarjete</div>
    </q-card>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  data: function () {
    return {
      n: 0,
      showBtn: true,
    };
  },
  methods: {
    aumentar() {
      this.n++;
    },
    restar() {
      this.n--;
    },
  },
});
</script>
