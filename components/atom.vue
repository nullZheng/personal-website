<template>
    <button class="hamburger-button " @click="toggleMenu">
        <div></div>
        <div></div>
        <div></div>
    </button>

    <div class="menu-overlay" :class="!isMenuOpen ? 'translate-x-[150%]' : 'translate-x-0'" v-if="isMenuOpen" @click="closeMenu">
        <ul class="menu-items">
            <button @click="scrollTo('about')">About</button>
            <button @click="scrollTo('work')">Work</button>
            <button @click="scrollTo('skills')">Skills</button>
            <button @click="scrollTo('contact')">Contact</button>
            <button>
                <a href="/resume.pdf" target="_blank">Resume</a>
            </button>
        </ul>
    </div>
</template>

<script setup lang="ts">
const isMenuOpen = ref(false);

function scrollTo(section: string) {
    const top: any = document.getElementById(section)?.offsetTop;
    scroll({ top: top - 100, behavior: 'smooth' });
    closeMenu();
}

function toggleMenu() {
    isMenuOpen.value = !isMenuOpen.value;
}

function closeMenu() {
    isMenuOpen.value = false;
}
</script>

<style scoped>
.hamburger-button {
    position: absolute;
    top: 2rem;
    right: 2rem;
    width: 30px;
    height: 30px;
    transition: all 300ms cubic-bezier(.61, .01, .42, 1);
    cursor: pointer;
    background: transparent;
    border: 0px;
    z-index: 1;
}

.menu-overlay {
    margin-top: -2rem;
    height: 100vh;
    width: 100vw;
    /* transform: translate(150%); */
    background-color: #0a192f;
    transition: transform 0.5s ease-in-out;
    border: none;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.menu-items {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    gap: 1rem;
}

div {
    height: 0px;
    border: 1.5px solid #fff;
    width: 22px;
    display: block;
    position: absolute;
    transition: all 300ms cubic-bezier(.61, .01, .42, 1);
    background: #fff;
}

button:hover {
    transition-delay: 100ms;
    transform: scale(1.1);
}

button:hover div:nth-child(3):before {
    width: 2px;
    height: 2px;
    border-radius: 50%;
    background: #F26451;
}

button:hover div {
    border: 2px solid #fff;
    height: 9px;
    border-radius: 50%;
    margin-left: -1px;
    margin-top: 2px;
    animation: atom 300ms linear 1;
    width: 25px;
    top: 0px;
    background: transparent;
}

button:focus {
    outline: 0px;
}

div:nth-child(1) {
    top: 0px;
}

div:nth-child(2) {
    top: 8px;
}

div:nth-child(3) {
    top: 16px;
}

div:nth-child(3):before {
    opacity: 0;
    animation: ball 1.5s linear infinite;
    content: '';
    border: 2px solid #fff;
    display: block;
    position: relative;
    top: 0.25px;
}

button:hover div:nth-child(1) {
    transform: rotate(-33deg);
}

button:hover div:nth-child(2) {
    transform: rotate(90deg);
}

button:hover div:nth-child(3) {
    transform: rotate(33deg);
}

button:hover div:nth-child(3):before {
    opacity: 1;
    transition: opacity 600ms cubic-bezier(.61, .01, .42, 1);
    ;
}

button:active:hover div:nth-child(3):before,
button:active div:nth-child(3):before,
button:active div:nth-child(2) {
    opacity: 0;
    transition: all 200ms;
}

button:active div {
    border: 1.5px solid #fff;
    height: 0px;
    border-radius: 0%;
    margin-left: -1px;
    margin-top: 6px;
    animation: division 300ms linear 1;
    width: 25px;
    top: 0px;
}

button:active div:nth-child(2) {
    width: 0px;
}

button:active div:nth-child(3) {
    transform: rotate(45deg);
}

button:active div:nth-child(1) {
    transform: rotate(-45deg);
}

@keyframes atom {
    0% {
        transform: rotate(180deg);
    }
}

@keyframes division {
    0% {
        transform: rotate(180deg);
    }
}

@keyframes ball {
    0% {
        left: -20%;
        top: 10%;
    }

    10% {
        left: 10%;
        top: -35%;
    }

    25% {
        left: 45%;
        top: -50%;
    }

    40% {
        left: 80%;
        top: -20%;
    }

    50% {
        left: 98%;
        top: 18%;
    }

    60% {
        left: 80%;
        top: 50%;
    }

    75% {
        left: 45%;
        top: 80%;
    }

    90% {
        left: 0%;
        top: 60%;
    }

    100% {
        left: -20%;
        top: 10%;
    }
}
</style>