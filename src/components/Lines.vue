<template>
    <div class="container">        
        <svg 
            class="word"
            viewBox="0 0 64 22" 
            xmlns="http://www.w3.org/2000/svg"
        >
            <defs>
                <linearGradient  id="Gradient1" spreadMethod="reflect" x1="0" y1="1" x2="1" y2="0">
                    <stop offset="0" stop-color="#F41D62"/>
                    <stop offset="0.6" stop-color="#383de1">
                        <animate
                            attributeName="offset"
                            values="0.6;1;0.6"
                            repeatCount="indefinite"
                            dur="2.5"
                            begin="0"
                            keySplines="0.65, 0, 0.35, 1;
                                        0.61, 1, 0.88, 1;"
                        />
                    </stop>
                </linearGradient >
            </defs>            

            <filter id="blur" x="-10%" y="-10%" width="120%" height="120%">
                <feGaussianBlur in="sourceGraphic" stdDeviation="0,0">
                    <animate
                        attributeName="stdDeviation"
                        values="0,0;0,0;1,0.1;0,0;"
                        repeatCount="indefinite"                        
                        dur="5"
                        begin="1"
                        keyTimes="0;0.7;0.85;1"
                        calcMode="spline"
                        keySplines="0.61, 1, 0.88, 1;
                                    0.65, 0, 0.35, 1;                                    
                                    0.61, 1, 0.88, 1;"
                    />
                </feGaussianBlur>
            </filter>

            <path 
                d="M 3.314 15.357 C 4.028 14.952 4.761 14.613 5.498 14.256 C 6.024 14.001 6.564 13.783 7.075 13.496 C 7.629 13.186 8.146 12.808 8.668 12.447 C 9.751 11.698 10.956 11.183 12.134 10.605 C 12.786 10.286 13.476 10.047 14.12 9.716 C 14.788 9.372 15.423 8.963 16.092 8.622 C 16.73 8.296 17.433 8.006 17.993 7.552 C 18.118 7.451 18.577 7.314 18.415 7.314 C 18.287 7.314 17.962 7.905 17.894 7.997 C 17.698 8.263 17.52 8.533 17.346 8.815 C 17.02 9.342 16.628 9.748 16.148 10.143 C 15.088 11.013 13.965 11.841 13.046 12.867 C 12.75 13.198 12.569 13.566 12.332 13.934 C 12.113 14.275 11.865 14.59 11.622 14.912 C 11.446 15.144 11.31 15.402 11.139 15.64 C 11.1 15.693 10.961 15.823 11.022 15.799 C 11.176 15.738 11.297 15.596 11.451 15.527 C 12.195 15.196 12.918 14.823 13.675 14.507 C 14.423 14.195 15.053 13.688 15.746 13.276 C 16.626 12.754 17.522 12.335 18.348 11.72 C 18.985 11.244 19.552 10.693 20.14 10.161 C 20.447 9.883 20.769 9.623 21.059 9.327 C 21.418 8.961 21.73 8.556 22.108 8.208 C 22.536 7.815 23.001 7.465 23.434 7.076 C 23.703 6.834 24.008 6.57 24.355 6.445 C 24.419 6.422 24.543 6.295 24.543 6.364 C 24.543 6.464 24.465 6.545 24.42 6.629 C 24.077 7.271 23.723 7.909 23.362 8.541 C 22.69 9.716 21.552 10.496 20.688 11.528 C 20.352 11.931 19.994 12.314 19.657 12.717 C 19.172 13.298 18.544 13.785 17.97 14.278 C 17.087 15.037 16.266 15.796 15.513 16.682 C 15.195 17.055 14.685 17.494 14.585 17.996 C 14.572 18.061 14.703 17.935 14.76 17.902 C 14.876 17.834 14.979 17.751 15.092 17.679 C 15.525 17.406 16.013 17.176 16.465 16.933 C 17.176 16.553 17.888 16.169 18.59 15.774 C 19.577 15.22 20.422 14.481 21.326 13.809 C 22.261 13.114 23.118 12.367 23.973 11.578 C 24.851 10.767 25.792 10.049 26.72 9.298 C 27.385 8.76 28.09 8.279 28.693 7.669 C 29.234 7.122 29.865 6.82 30.51 6.42 C 30.954 6.144 31.386 5.819 31.844 5.569 C 31.954 5.509 31.995 5.466 31.981 5.634 C 31.956 5.958 31.605 6.313 31.458 6.591 C 31.177 7.122 30.963 7.682 30.694 8.217 C 30.327 8.947 29.845 9.606 29.387 10.28 C 28.824 11.107 28.223 11.854 27.576 12.616 C 26.88 13.437 26.243 14.305 25.556 15.134 C 24.706 16.161 23.863 17.19 23.016 18.218 C 22.834 18.44 22.651 18.642 22.45 18.843 C 22.38 18.912 22.221 19.008 22.196 19.095 C 22.167 19.197 22.322 18.958 22.362 18.919 C 22.972 18.335 23.657 17.848 24.382 17.419 C 25.283 16.885 26.169 16.332 27.077 15.808 C 28.31 15.097 29.562 14.45 30.663 13.537 C 31.416 12.911 32.061 12.219 32.694 11.475 C 33.306 10.754 33.956 10.148 34.715 9.583 C 36.002 8.625 37.193 7.529 38.505 6.609 C 39.075 6.209 39.652 5.86 40.309 5.634 C 40.323 5.629 40.561 5.534 40.531 5.598 C 40.414 5.856 40.184 6.054 40.039 6.299 C 39.844 6.628 39.67 6.973 39.505 7.319 C 39.113 8.142 38.555 8.864 38.126 9.668 C 36.971 11.83 35.879 14.012 34.59 16.098 C 34.262 16.628 33.911 17.135 33.592 17.67 C 33.441 17.924 33.182 18.195 33.125 18.493 C 33.107 18.584 33.043 18.705 33.093 18.551 C 33.238 18.108 33.681 17.727 33.976 17.387 C 34.697 16.56 35.44 15.772 36.263 15.044 C 37.362 14.072 38.498 13.16 39.451 12.036 C 40.257 11.086 40.896 10.041 41.585 9.008 C 41.877 8.569 42.194 8.147 42.475 7.701 C 42.785 7.208 43.059 6.692 43.385 6.209 C 44.091 5.16 45.166 4.561 46.078 3.72 C 46.286 3.528 46.47 3.307 46.675 3.111 C 46.769 3.022 46.739 3.049 46.743 3.154 C 46.749 3.323 46.792 3.473 46.774 3.648 C 46.73 4.086 46.615 4.526 46.541 4.96 C 46.201 6.951 45.375 8.873 44.609 10.729 C 44.014 12.169 43.42 13.608 42.91 15.082 C 42.725 15.619 42.491 16.123 42.223 16.623 C 42.054 16.939 41.787 17.242 41.693 17.594 C 41.679 17.644 41.657 17.672 41.646 17.722 C 41.624 17.822 41.528 17.836 41.603 17.724 C 41.88 17.313 42.353 16.944 42.717 16.619 C 43.687 15.754 44.655 14.894 45.608 14.011 C 46.059 13.593 46.537 13.201 46.963 12.757 C 47.286 12.421 47.557 12.043 47.855 11.686 C 48.324 11.123 48.866 10.612 49.41 10.122 C 49.801 9.769 50.169 9.422 50.524 9.033 C 50.777 8.755 50.948 8.458 51.16 8.15 C 51.445 7.734 51.699 7.359 52.078 7.024 C 52.292 6.836 52.486 6.621 52.687 6.42 C 52.94 6.168 53.29 6.035 53.604 5.872 C 53.889 5.724 54.123 5.41 54.417 5.297 C 54.567 5.239 54.628 5.265 54.628 5.45 C 54.628 5.816 54.514 6.067 54.408 6.42 C 54.221 7.041 53.963 7.638 53.747 8.249 C 53.249 9.663 52.803 11.088 52.249 12.483 C 51.527 14.304 51.001 16.272 49.944 17.933 C 49.79 18.175 49.612 18.471 49.398 18.666 C 49.352 18.708 49.7 18.232 49.758 18.174 C 50.311 17.623 50.979 17.201 51.613 16.754 C 52.745 15.956 53.807 15.087 54.871 14.202 C 56.029 13.238 57.214 12.314 58.407 11.394 C 59.019 10.921 59.643 10.458 60.132 9.853 C 60.371 9.557 60.628 9.293 60.887 9.015 C 60.909 8.991 61.057 8.797 61.057 8.846" 
                stroke="url(#Gradient1)"
                fill="none"
                stroke-width="5"
                stroke-linecap="round" 
                stroke-linejoin="round"
                stroke-dashoffset="230" 
                stroke-dasharray="230"
                class="lines"
                :style="{ transform: 'translate(' + -mouseTransform.x * 0.75 + 'px, ' + -mouseTransform.y * 0.75 + 'px)  scale(0.8)'}"
            >
                <animate
                    attributeName="stroke-dashoffset" 
                    values="230;0;0;-230"
                    begin="0"
                    dur="5"
                    repeatCount="indefinite"
                    keySplines="0.65, 0, 0.35, 1;
                                0.61, 1, 0.88, 1; 
                                0.61, 1, 0.88, 1;"
                    keyTimes="0; 0.4; 0.7; 1"
                    calcMode="spline"
                />
            </path>
            
            <g filter="url(#blur)">               
                <text 
                    x="50%" y="50%" 
                    dominant-baseline="central" 
                    class="text" 
                    text-anchor="middle"
                    fill="#0ff"
                    :style="{ transform: 'translate(' + mouseTransform.x * 0.5 + 'px, ' + mouseTransform.y * 0.5 + 'px)'}"                    
                >
                    {{ words[currentWord] }}
                </text>
                <text 
                    x="50%" y="50%" 
                    dominant-baseline="central" 
                    class="text" 
                    text-anchor="middle"
                    fill="#f0f"
                    :style="{ transform: 'translate(' + mouseTransform.x * 0.1 + 'px, ' + mouseTransform.y * 0.1 + 'px)'}"                    
                >
                    {{ words[currentWord] }}
                </text>
                <text 
                    x="50%" y="50%" 
                    dominant-baseline="central" 
                    class="text"
                    fill="#e6e6e6" 
                    text-anchor="middle"
                    :style="{ transform: 'translate(' + mouseTransform.x * 0.3 + 'px, ' + mouseTransform.y * 0.3 + 'px)'}"                    
                >
                    {{ words[currentWord] }}
                </text>
            </g>            
        </svg>
    </div>
</template>

<script>
export default {
    props: {
        mouse: {
            type: Object
        }
    },
    data() {
        return {
            currentWord: 0,
            words: [
                'SENNERY',
                'MODERN',
                'CLEAN',
                'AESTHETIC'
            ],

            mouseTransform: {
                x: 0,
                y: 0,
                filter: 0
            },
            speed: 1
        }
    },
    computed: {
        center() {
            const x = document.documentElement.clientWidth / 2;
            const y = document.documentElement.clientHeight / 2;

            return { x, y }
        },
        maxDistance() {
            const x = document.documentElement.clientWidth;
            const y = document.documentElement.clientHeight;

            return Math.sqrt(x*x + y*y) / 2;
        }
    },
    methods: {
        moveObj() {
            const mouse = this.mouse;
            const vMouse = {
                vx: this.center.x - mouse.x,
                vy: this.center.y - mouse.y,                
            }
            const distance = Math.sqrt(vMouse.vx * vMouse.vx + vMouse.vy * vMouse.vy);
            const vMouseNormalized = {
                vx: vMouse.vx / distance,
                vy: vMouse.vy / distance,
            };
            const speed = this.speed * distance / this.maxDistance;
            //const angle = Math.atan2(mouse.y - this.center.y, mouse.x - this.center.x);

            this.mouseTransform.x = vMouseNormalized.vx * speed;
            this.mouseTransform.y = vMouseNormalized.vy * speed;
            this.mouseTransform.filter = vMouseNormalized.vy * speed * 0.1;
            //this.mouseTransform.skewX = angle;
            //this.mouseTransform.skewY = angle;
        }
    },
    mounted() {
        setInterval(this.moveObj, 15);
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
}

.word {
    width: 80vw;
    transition: transform 1s ease-out;
}

.lines {
    transform-origin: center;
}

.infinity {
    position: absolute;
    z-index: -99;
    height: 100vh;
}

.text {
    font-size: 10px;
    font-weight: bold;
} 
</style>