<template>
    <div class="game-loader">
        <div class="game-loader__planet">
            <div class="loader-radius1"></div>
            <div class="loader-radius2"></div>
            <div class="loader-radius3"></div>
            <div class="loader-radius4"></div>
            <div class="loader-mini1"></div>
            <div class="loader-mini2"></div>
            <div class="loader-mini3"></div>
            <div class="loader-mini4"></div>
            <svg xmlns="http://www.w3.org/2000/svg" version="1.1">
                <defs>
                    <filter id="goo">
                    </filter>
                </defs>
            </svg>
        </div>
    </div>
</template>

<style scoped>
.game-loader {
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10000;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
    background-color: #0a192f;
}

.game-loader__planet {
    filter: url("#goo");
    position: relative;
    width: 100vw;
    height: 100vw;
}

.game-loader__planet::after {
    content: "";
    display: block;
    width: 8vw;
    height: 8vw;
    border-radius: 50%;
    background: #11DBD9;
    box-shadow: #11DBD9 0 0 24px 4px;
    margin: 0 auto;
    position: absolute;
    top: 46vw;
    left: 46vw;
    -webkit-animation: scale 4s linear infinite, color5 2s linear 1;
    animation: scale 4s linear infinite, color5 2s linear 1;
}

.game-loader__planet .loader-mini1 {
    position: absolute;
    width: 3vw;
    height: 3vw;
    border-radius: 50%;
    background: #11DBD9;
    top: 48.5vw;
    left: 48.5vw;
    -webkit-animation: move1 2s linear 1, color1 2s linear 1;
    animation: move1 2s linear 1, color1 2s linear 1;
}

.game-loader__planet .loader-mini2 {
    position: absolute;
    width: 3.6vw;
    height: 3.6vw;
    border-radius: 50%;
    background: #11DBD9;
    top: 48.5vw;
    left: 48.5vw;
    -webkit-animation: move2 2.25s linear 1, color2 2.25s linear 1;
    animation: move2 2.25s linear 1, color2 2.25s linear 1;
}

.game-loader__planet .loader-mini3 {
    position: absolute;
    width: 4.2vw;
    height: 4.2vw;
    border-radius: 50%;
    background: #11DBD9;
    top: 48.5vw;
    left: 48.5vw;
    -webkit-animation: move3 2.5s linear 1, color3 2.5s linear 1;
    animation: move3 2.5s linear 1, color3 2.5s linear 1;
}

.game-loader__planet .loader-mini4 {
    position: absolute;
    width: 4.8vw;
    height: 4.8vw;
    border-radius: 50%;
    background: #11DBD9;
    top: 48.5vw;
    left: 48.5vw;
    -webkit-animation: move4 2.75s linear 1, color4 2.75s linear 1;
    animation: move4 2.75s linear 1, color4 2.75s linear 1;
}

.game-loader__planet .loader-radius1 {
    position: absolute;
    width: 12vw;
    height: 12vw;
    border-radius: 50%;
    border: 0.5px solid #11DBD9;
    opacity: 0.2;
    background: transparent;
    top: 44vw;
    left: 44vw;
    transform: scale(0);
    -webkit-animation: orbit1 2s linear 1;
    animation: orbit1 2s linear 1;
}

.game-loader__planet .loader-radius2 {
    position: absolute;
    width: 18vw;
    height: 18vw;
    border-radius: 50%;
    border: 0.5px solid #11DBD9;
    opacity: 0.2;
    background: transparent;
    transform: scale(0);
    top: 41vw;
    left: 41vw;
    -webkit-animation: orbit2 2.25s linear 1;
    animation: orbit2 2.25s linear 1;
}

.game-loader__planet .loader-radius3 {
    position: absolute;
    width: 24vw;
    height: 24vw;
    border-radius: 50%;
    border: 0.5px solid #11DBD9;
    opacity: 0.2;
    background: transparent;
    transform: scale(0);
    top: 38vw;
    left: 38vw;
    -webkit-animation: orbit3 2.5s linear 1;
    animation: orbit3 2.5s linear 1;
}

.game-loader__planet .loader-radius4 {
    position: absolute;
    width: 30vw;
    height: 30vw;
    border-radius: 50%;
    border: 0.5px solid #11DBD9;
    opacity: 0.2;
    background: transparent;
    transform: scale(0);
    top: 35vw;
    left: 35vw;
    -webkit-animation: orbit4 2.75s linear 1;
    animation: orbit4 2.75s linear 1;
}

.game-loader__planet--color .loader-mini1 {
    background: #0fc3c2;
}

.game-loader__planet--color .loader-mini2 {
    background: #0dacaa;
}

.game-loader__planet--color .loader-mini3 {
    background: #0b9493;
}

.game-loader__planet--color .loader-mini4 {
    background: #0a7c7b;
}

.btn-play {
    left: 41vw;
}

@-webkit-keyframes move1 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-6vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-12vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-12vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-12vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-6vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@keyframes move1 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-6vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-12vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-12vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-12vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-6vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@-webkit-keyframes move2 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-9vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-18vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-18vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-18vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-9vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@keyframes move2 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-9vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-18vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-18vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-18vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-9vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@-webkit-keyframes move3 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-12vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-24vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-24vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-24vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-12vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@keyframes move3 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-12vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-24vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-24vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-24vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-12vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@-webkit-keyframes move4 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-15vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-30vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-30vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-30vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-15vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@keyframes move4 {
    0% {
        transform: skewX(5deg) rotate(0deg) translateY(0em) rotate(0deg) skewX(-5deg) rotate(0deg);
    }

    10% {
        transform: skewX(5deg) rotate(180deg) translateY(-15vw) rotate(-180deg) skewX(-5deg) rotate(180deg);
    }

    25% {
        transform: skewX(5deg) rotate(360deg) translateY(-30vw) rotate(-360deg) skewX(-5deg) rotate(360deg);
    }

    50% {
        transform: skewX(5deg) rotate(720deg) translateY(-30vw) rotate(720deg) skewX(-5deg) rotate(720deg);
    }

    75% {
        transform: skewX(5deg) rotate(1080deg) translateY(-30vw) rotate(-1080deg) skewX(-5deg) rotate(1080deg);
    }

    90% {
        transform: skewX(5deg) rotate(1260deg) translateY(-15vw) rotate(-1260deg) skewX(-5deg) rotate(1260deg);
    }

    100% {
        transform: skewX(5deg) rotate(1440deg) translateY(0em) rotate(-1440deg) skewX(-5deg) rotate(1440deg);
    }
}

@-webkit-keyframes scale {
    0% {
        transform: scale(1.5);
    }

    50% {
        transform: scale(1);
    }

    100% {
        transform: scale(1.5);
    }
}

@keyframes scale {
    0% {
        transform: scale(1.5);
    }

    50% {
        transform: scale(1);
    }

    100% {
        transform: scale(1.5);
    }
}

@-webkit-keyframes orbit1 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@keyframes orbit1 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@-webkit-keyframes orbit2 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@keyframes orbit2 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@-webkit-keyframes orbit3 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@keyframes orbit3 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@-webkit-keyframes orbit4 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@keyframes orbit4 {
    0% {
        transform: scale(0);
    }

    10% {
        transform: scale(1);
    }

    25% {
        transform: scale(2.2);
    }

    35% {
        transform: scale(2.1);
    }

    50% {
        transform: scale(2);
    }

    65% {
        transform: scale(2.1);
    }

    75% {
        transform: scale(2);
    }

    90% {
        transform: scale(1);
    }

    100% {
        transform: scale(0);
    }
}

@-webkit-keyframes color1 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #FF217B;
    }

    90% {
        background: #11DBD9;
    }
}

@keyframes color1 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #FF217B;
    }

    90% {
        background: #11DBD9;
    }
}

@-webkit-keyframes color2 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #FF7878;
    }

    90% {
        background: #11DBD9;
    }
}

@keyframes color2 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #FF7878;
    }

    90% {
        background: #11DBD9;
    }
}

@-webkit-keyframes color3 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #FFA283;
    }

    90% {
        background: #11DBD9;
    }
}

@keyframes color3 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #FFA283;
    }

    90% {
        background: #11DBD9;
    }
}

@-webkit-keyframes color4 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #962A4E;
    }

    90% {
        background: #11DBD9;
    }
}

@keyframes color4 {
    10% {
        background: #11DBD9;
    }

    50% {
        background: #962A4E;
    }

    90% {
        background: #11DBD9;
    }
}

@-webkit-keyframes color5 {
    10% {
        background: #11DBD9;
        box-shadow: #11DBD9 0 0 24px 4px;
    }

    50% {
        background: #13C2D3;
        box-shadow: #13C2D3 0 0 24px 4px;
    }

    90% {
        background: #11DBD9;
        box-shadow: #11DBD9 0 0 24px 4px;
    }
}

@keyframes color5 {
    10% {
        background: #11DBD9;
        box-shadow: #11DBD9 0 0 24px 4px;
    }

    50% {
        background: #13C2D3;
        box-shadow: #13C2D3 0 0 24px 4px;
    }

    90% {
        background: #11DBD9;
        box-shadow: #11DBD9 0 0 24px 4px;
    }
}

.game-loader {
    width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10000;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
}

svg {
    position: absolute;
    z-index: -100;
    pointer-events: none;
}</style>