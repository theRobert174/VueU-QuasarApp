<template>
  <q-page class="q-ma-md">
    <span class="text-h3">Forms</span>
    <q-separator spaced/>

    <div class="row justify-center">
        <q-form
          @submit="onSubmit"
          @reset="onReset"
          class="q-gutter-xs col-xs-12 col-sm-12 col-md-6 q-pt-t"
        >
          <q-input
            filled
            type="email"
            v-model="name"
            label="Email *"
            lazy-rules
            :rules="[ val => val && val.length > 0 || 'El campo es obligatorio']"
          />

          <q-input
            filled
            type="password"
            v-model="age"
            label="Password *"
            lazy-rules
            :rules="[ val => val && val.length > 0 || 'El campo es obligatorio']"
          />

          <q-input
            filled
            type="password"
            v-model="age"
            label="Repeat password *"
            lazy-rules
            :rules="[ val => val && val.length > 0 || 'El campo es obligatorio']"
          />

          <div class="row justify-end">
            <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
            <q-btn unelevated label="Submit" type="submit" color="primary"/>
          </div>
        </q-form>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";
import { useQuasar } from 'quasar'

export default defineComponent({
  name: "FormsPage",
});
</script>
