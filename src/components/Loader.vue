<template>
    <div 
        class="container"
    >
        <div
            class="signs"
        >
            <!-- <svg 
                class="loader" 
                viewBox="0 0 41 20" 
                fill="none" 
                xmlns="http://www.w3.org/2000/svg"
                v-for="(elem, i) in signs"
                :key="'inf' + i"
                :style="{ 
                    transform: 'translate(' + elem.transform.x + 'vw ,' + elem.transform.y + 'vh)' +
                        'scale(' + findScale(elem.transform.x, elem.transform.y) + ')' 
                }"
            >
                <path 
                    d="M 20.5 10 L 14.216 4.414 C 11.384 1.897 7.116 1.897 4.284 4.414 C 0.94 7.387 0.94 12.613 4.284 15.586 C 7.116 18.103 11.384 18.103 14.216 15.586 L 20.5 10 Z M 20.5 10 L 26.785 15.586 C 29.616 18.103 33.884 18.103 36.715 15.586 C 40.06 12.613 40.06 7.387 36.715 4.414 C 33.884 1.897 29.616 1.897 26.784 4.414 C 24.842 6.141 22.978 7.797 20.5 10 Z" 
                    stroke="#17181c" 
                    stroke-width="2" 
                    stroke-dasharray="0 52 0"
                >
                    <animate
                        :id="'inf' + i" 
                        attributeName="stroke-dashoffset" 
                        values="0;104;"
                        :dur="duration"
                        :keySplines="elem.timeFunc"
                        calcMode="spline"
                    />
                    <animate
                        attributeName="stroke-width"
                        values="0;2;0"
                        :begin="'inf' + i + '.begin'"
                        :end="'inf' + i + '.end'"
                        :dur="duration"
                        keySplines=".25 .1 .25 1;
                                    .12 0 .39 0;"
                        calcMode="spline"
                    />
                </path>
            </svg> -->
            <svg 
                class="loader s" 
                viewBox="0 0 41 20" 
                fill="none" 
                xmlns="http://www.w3.org/2000/svg"
            >
                <path 
                    d="M1 2L17 18L24 2L40 18" 
                    stroke="url(#Gradient1)" 
                    stroke-width="2" 
                    stroke-dashoffset="32" 
                    stroke-dasharray="0 32" 
                >
                    <animate
                        id="s" 
                        attributeName="stroke-dasharray" 
                        values="0 32;64 0;"
                        :dur="duration" 
                        repeatCount="indefinite"
                        keySplines=".25 .1 .25 1;"
                        calcMode="spline"
                    />
                </path>                
            </svg>
            <svg 
                class="loader background"
                viewBox="0 0 200 200" 
                xmlns="http://www.w3.org/2000/svg"
            >
                <defs>
                    <mask id="mask" class="background">
                        <rect x="0" y="0" width="200" height="200" fill="#fff"/>
                        <path 
                            d="M34.7,-64.7C38.5,-57.8,30.9,-35.6,33.4,-22.3C35.9,-9,48.5,-4.5,49.2,0.4C49.8,5.2,38.4,10.4,29.4,12.4C20.3,14.3,13.5,13,9,23.9C4.5,34.7,2.3,57.7,-0.6,58.8C-3.6,60,-7.1,39.2,-19,32.6C-30.9,26.1,-51.2,33.7,-54.7,30.6C-58.1,27.5,-44.8,13.8,-43.5,0.7C-42.2,-12.3,-53,-24.6,-49.5,-27.4C-45.9,-30.3,-27.9,-23.7,-17.2,-26.7C-6.6,-29.8,-3.3,-42.4,6,-52.9C15.4,-63.3,30.8,-71.6,34.7,-64.7Z" 
                            transform="translate(100 100) scale(0)"
                        >
                            <animate
                                id="backPath" 
                                attributeName="d" 
                                values="M34.7,-64.7C38.5,-57.8,30.9,-35.6,33.4,-22.3C35.9,-9,48.5,-4.5,49.2,0.4C49.8,5.2,38.4,10.4,29.4,12.4C20.3,14.3,13.5,13,9,23.9C4.5,34.7,2.3,57.7,-0.6,58.8C-3.6,60,-7.1,39.2,-19,32.6C-30.9,26.1,-51.2,33.7,-54.7,30.6C-58.1,27.5,-44.8,13.8,-43.5,0.7C-42.2,-12.3,-53,-24.6,-49.5,-27.4C-45.9,-30.3,-27.9,-23.7,-17.2,-26.7C-6.6,-29.8,-3.3,-42.4,6,-52.9C15.4,-63.3,30.8,-71.6,34.7,-64.7Z;
                                        M35.4,-62.1C44.6,-55.9,50.2,-44,57.5,-32.7C64.9,-21.4,74,-10.7,75.2,0.7C76.3,12,69.4,24,63.5,37.9C57.6,51.7,52.7,67.3,42.3,71.5C31.9,75.7,15.9,68.5,1.8,65.5C-12.4,62.5,-24.9,63.5,-33.4,58.2C-41.9,52.9,-46.4,41.2,-52.9,30.4C-59.5,19.6,-68,9.8,-71.4,-2C-74.8,-13.7,-73,-27.4,-67.7,-40.4C-62.4,-53.3,-53.7,-65.5,-41.8,-70.2C-29.9,-74.9,-15,-72.1,-1,-70.4C13,-68.8,26.1,-68.3,35.4,-62.1Z;"
                                begin="indefinite"
                                :dur="duration" 
                                keySplines="0.5, 1, 0.89, 1"
                                calcMode="spline"
                                fill="freeze"
                            />
                            <animateTransform
                                id="backTranslate"
                                attributeName="transform" 
                                type="translate" 
                                from="100,100" 
                                to="100,100" 
                                begin="backPath.begin"
                                additive="replace"
                                :dur="duration" 
                                keySplines=".25 .1 .25 1;"
                                calcMode="spline"
                                fill="freeze"
                            />
                            <animateTransform
                                id="backScale"
                                attributeName="transform" 
                                type="scale" 
                                from="0" 
                                to="1" 
                                begin="backPath.begin"
                                additive="sum"
                                :dur="duration" 
                                keySplines="0.5, 1, 0.89, 1;"
                                calcMode="spline"
                                fill="freeze"
                            />
                        </path>
                    </mask>
                </defs>
                
                <rect class="rect" x="0" y="0" width="200" height="200" fill-opacity="1" fill="white" mask="url(#mask)" />
            </svg>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Loader',
    props: {
    },
    data() {
        return {
            duration: 0.75,

            signs: [                
                {
                    timeFunc: '.11 0 .5 0;',
                    transform: {
                        x: '0',
                        y: '0',  
                    }
                },
                {
                    timeFunc: '.45 0 .55 0;',
                    transform: {
                        x: '+35',
                        y: '-15',
                    }
                },
                {
                    timeFunc: '.25 .1 .25 1;',
                    transform: {
                        x: '20',
                        y: '15',
                    }
                },
                {
                    timeFunc: '.7 0 .84 0;',
                    transform: {
                        x: '-10',
                        y: '-35',
                    }
                },
                {
                    timeFunc: '.85 0 .15 0;',
                    transform: {
                        x: '-20',
                        y: '30', 
                    }
                },
                {
                    timeFunc: '.16 1 .3 1;',
                    transform: {
                        x: '-35',
                        y: '-15',
                    }
                },
            ]
        }
    },
    methods: {
        findScale(x,y) {
            const scale = 1 - (Math.abs(x) + Math.abs(y))/100;
            return scale;
        },
    },
    created() {
        window.addEventListener('load', () => {
            setTimeout(() => {
                document.getElementById('s').setAttribute('repeatCount', '1');
                document.getElementById('backPath').beginElement();
            },this.duration * 1000)            
            console.log('loaded!');
        })
    }
}
</script>

<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    overflow: hidden;  
    z-index: 9998;
}

.signs {
    height: 15vh;
    width: 30.75vh;
}

.loader {
    position: absolute;
    height: 15vh;
    transition: transform 0.5s cubic-bezier(0.65, 0, 0.35, 1);
}

.s {   
    transform: rotateZ(-90deg);
}

.background {
    z-index: -999;
    height: 100vh;
    width: 100vw;
    top: 0;
    left: 0;
}

.background .rect {
    transform-origin: center;
    transform: scale(4);
}
</style>
