<template>
    <div id="app">
            <!-- app content -->
    </div>
</template>

<script>
    export default {
        name: 'app'
    }
</script>

<style>

/* vue-print-styles Copyright 2018, Eiseins */
/* MIT license, see following website for details */
/* https://github.com/eiseins/vue-print-styles */
    @media print {
        /* This is not an exhaustive set of elements and classes that need to be styled for printing. */
        /* You will likely need to add more depending on your app. */

        /* Standard HTML Elements */
        aside, nav { display: none !important; }
        footer { display: none !important; }
        body * { color: black !important; background-color: white !important; }
        h1, h2, h3, h4, h5, h6 {
            page-break-inside: avoid;
            page-break-after: avoid;
        }
        main {
            padding: 0 !important;
        }

        /* Vuetify specific classes.  Used because vue converts custom elements to standard ones with special classes. */
        /* WARNING these are brittle because these classes can easily change in future versions of Vuetify. */
        .layout, .card, .card__content {
            box-shadow: unset !important;
            -webkit-box-shadow: unset !important;
            border-radius: unset !important;
        }
        .carousel__left, .carousel__right, .carousel__controls {
            display: none !important;
        }
        .grey--text{ color: black !important; }
        .chip--outline{ border-color: black !important; }


        /* Pseudo Classes */
        a:link          { color: black !important; text-decoration:none; }
        a:visited       { color: black !important; text-decoration:none; }
        a:hover         { color: black !important; text-decoration:none; }
        a:active        { color: black !important; text-decoration:none; }

        /* Utility Classes */
        .print-together {
            page-break-inside: avoid;
        }
        /* Use .print-no to hide buttons or controls. Alternately you can use display: none on all control classes like carousel above. */
        .print-no { display: none !important; }
        .print-break-after { page-break-after: always !important; }

    }

    @media screen {
        .screen-no{ display: none !important }
    }
/* end vue-print-styles */

</style>
