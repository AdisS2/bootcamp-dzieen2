<template>
    <div>
        <button @click="pobierzWpisy">refresh</button>
        siema blog!
        {{ wpisy }}
    </div>
</template>

<script>
import { dzieen2_backend } from 'declarations/dzieen2_backend/index';

export default {
    data () {
        return {
            wpisy:[]
        }
    },
    methods: {
        async pobierzWpisy() {
            this.wpisy = await dzieen2_backend.odczytaj_wpisy();
        }
    },
}
</script>