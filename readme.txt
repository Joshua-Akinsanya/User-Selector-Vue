# Installation
In project directory run:
    npm create vite@latest .

// Curent version of vite: vite@8.0.1

Select a framework:
Vue

Select a variant:
TypeScript

Use a rolldown-vite (Experimental)?:
No

Install with npm and start now?
Yes

npm install vuetify
source: vuetify.js.com

add code to main.ts:

-----------

// Vuetify
import 'vuetify/styles/main.css'
import { createVuetify } from 'vuetify'
import * as components from 'vuetify/components'
import * as directives from 'vuetify/directives'

const vuetify = createVuetify({
    components,
    directives,
})

createApp(App).use(vuetify).mount('#app')

---------------

add code to package.json file for type checking in '.vue' files:
"type-check": "vue-tsc --noEmit" // No emit to prevent generation of js files

