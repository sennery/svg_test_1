<template>
    <div id="app" @mousemove="mouseMove" v-scroll="{ progressFunc: progressFunction, getter: getScroll }">
        <Loader/>
        <div class="hide wrapper">            
            <Lines 
                :mouse="mouse"
            />
            <Works
                v-for="i in [1,2,3,4,5]"
                :key="i"
            />
            <About/>
            <Transition
                :scroll="scroll"
            />
        </div>
    </div>
</template>

<script>
import Loader from './components/Loader.vue'
import Lines from './components/Lines.vue'
import Works from './components/Works.vue'
import About from './components/About.vue'
import Transition from './components/Transition.vue'

export default {
    name: 'App',
    components: {
        Loader,
        Lines,
        Works,
        About,
        Transition
    },
    data() {
        return {
            mouse: {
                x: 0,
                y: 0
            },

            scroll: {}
        }
    },
    methods: {
        mouseMove(e) {
            this.mouse.x = e.pageX;
            this.mouse.y = e.pageY;
        },
        progressFunction(part) {
            return 1 - Math.pow(1 - part, 2);
        },
        getScroll(scroll) {
            this.scroll = scroll;
        }
    },
    created() {
        window.addEventListener('load', () => {
            document.querySelector('.wrapper').classList.remove('hide');      
            console.log('loaded!');
        })
    }
}
</script>

<style>
html {
    font-family: "Anodina", sans-serif;
    font-size: 1vw;
    line-height: 1;
    background-color: #17181c !important;
    background-image: url('./assets/123.jpg');
    overflow: hidden;   
}

body {
    position: absolute;
    top: 0;
    left: 0;
    filter: url(#transitionFilter);
}

#app {
    position: absolute;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;  
}

.wrapper {
    transition: transform 0.75s cubic-bezier(0.5, 1, 0.89, 1) 0.75s; 
    transform-origin: 50% 50vh;
}

.hide {
    transform: scale(0) !important;
}

@font-face {
    font-family: "Anodina";
    src: url("assets/fonts/Anodina-Light.otf");
    font-weight: normal;
}
@font-face {
    font-family: "Anodina";
    src: url("assets/fonts/Anodina-ExtraBold.otf");
    font-weight: bold;
}
html, body, body div, span, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, pre, abbr, address, cite, code, del, dfn, em, img, ins, kbd, q, samp, small, strong, sub, sup, var, b, i, dl, dt, dd, ol, ul, li, fieldset, form, label, legend, table, caption, tbody, tfoot, thead, tr, th, td, article, aside, figure, footer, header, menu, nav, section, time, mark, audio, video, details, summary {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font-weight: normal;
	vertical-align: baseline;
	background: transparent;
}

article, aside, figure, footer, header, nav, section, details, summary {display: block;}

html {
	box-sizing: border-box;
}

*,
*:before,
*:after {
	box-sizing: inherit;
}
*/
img,
object,
embed {max-width: 100%;}

ul {list-style: none;}

blockquote, q {quotes: none;}

blockquote:before,
blockquote:after,
q:before,
q:after {content: ''; content: none;}

a {margin: 0; padding: 0; font-size: 100%; vertical-align: baseline; background: transparent;}

del {text-decoration: line-through;}

abbr[title], dfn[title] {border-bottom: 1px dotted #000; cursor: help;}

table {border-collapse: collapse; border-spacing: 0;}
th {font-weight: bold; vertical-align: bottom;}
td {font-weight: normal; vertical-align: top;}

hr {display: block; height: 1px; border: 0; border-top: 1px solid #ccc; margin: 1em 0; padding: 0;}

input, select {vertical-align: middle;}

pre {
    white-space: pre; 
    white-space: pre-wrap; 
    white-space: pre-line; 
    word-wrap: break-word; 
}

input[type="radio"] {vertical-align: text-bottom;}
input[type="checkbox"] {vertical-align: bottom;}
.ie7 input[type="checkbox"] {vertical-align: baseline;}
.ie6 input {vertical-align: text-bottom;}

select, input, textarea {font: 99% sans-serif;}

table {font-size: inherit; font: 100%;}

small {font-size: 85%;}

strong {font-weight: bold;}

td, td img {vertical-align: top;}

sub, sup {font-size: 75%; line-height: 0; position: relative;}
sup {top: -0.5em;}
sub {bottom: -0.25em;}

pre, code, kbd, samp {font-family: monospace, sans-serif;}
.clickable,
label,
input[type=button],
input[type=submit],
input[type=file],
button {cursor: pointer;}

button, input, select, textarea {margin: 0;}
button,
input[type=button] {width: auto; overflow: visible;}
.ie7 img {-ms-interpolation-mode: bicubic;}
.clearfix:before, .clearfix:after { content: "\0020"; display: block; height: 0; overflow: hidden; }
.clearfix:after { clear: both; }
.clearfix { zoom: 1; }
</style>
