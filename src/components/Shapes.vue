<script>
export default {
    computed: {
        basicMath() {
            return Math.floor(Math.random() * 900)
        },
    },
}
</script>

<template>
    <div class="shape-container" :style="{ overflow: 'hidden' }">
        <svg
            class="svg-shapes"
            xmlns="http://www.w3.org/2000/svg"
            version="1.1"
            viewBox="100 100 600 600"
            preserveAspectRatio="xMidYMid slice"
        >
            <!-- put 4 of these in an array and call list array -->
            <circle
                key="0"
                r="{{basicMath + 100}}"
                cx="{{basicMath}}"
                cy="{{basicMath)}}"
                stroke-width="{{Math.floor(Math.random() * 200 + 75)}}"
                stroke-dasharray="{{`${getRandomLength()} ${getRandomGap()}`}}"
            />
        </svg>
        <svg :style="{ pointerEvents: 'none' }">
            <defs>
                <linearGradient id="bggrad" x1="0%" y1="0%" x2="100%" y2="100%">
                    <stop offset="0%" :style="{ stopColor: '#E9336B' }" />
                    <stop offset="100%" :style="{ stopColor: '#ff8674' }" />
                </linearGradient>
            </defs>
        </svg>
    </div>
</template>
<style scoped>
.shape-container {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    width: 100vw;
    height: 100vh;
}

.svg-shapes {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100vw;
    height: 100%;
    margin: 0;
}

.svg-shapes circle {
    fill: transparent;
    stroke: url(#bggrad);
    stroke-linecap: round;
    animation: bgmove 200s linear infinite;
}

@keyframes bgmove {
    0% {
        stroke-dashoffset: 1000;
    }

    100% {
        stroke-dashoffset: 0;
    }
}
</style>
