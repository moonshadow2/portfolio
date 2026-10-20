<body class="bg-black dark:black">
    <div class="min-h-screen flex flex-col justify-center items-center">
        <div class="scene mb-12">
            <div class="bowl">
                <div class="liquid"></div>
            </div>
        </div>
        <h1 class="liquid-text liquid-text-inverse text-4xl md:text-5xl lg:text-6xl font-bold text-center mb-4">
        Portfolio is under construction
        </h1>

        <p class="liquid-text liquid-text-inverse text-center text-lg md:text-xl lg:text-2xl mb-8">
            Please try again soon!
        </p>
        <div class="flex gap-6 text-lg">
            <a href="https://github.com/moonshadow2" class="liquid-text hover:underline">GitHub</a>
            <a href="https://www.linkedin.com/in/savar-shrestha/" class="liquid-text hover:underline">LinkedIn</a>
            <a href="savarshrestha18@gmail.com" class="liquid-text hover:underline">Email</a>
        </div>
    </div>
</body>

<style>
    .scene {
        position: relative;
        width: 300px;
        height: 300px;
    }

    .bowl {
        position: relative;
        width: 300px;
        height: 300px;
        background: rgba(255, 255, 255, 0.1);
        border-radius: 50%;
        border: 8px solid transparent;
        animation: animate 5s linear infinite;
        transform-origin: bottom center;
    }

    @keyframes animate {
        0% { transform: rotate(0deg); }
        25% { transform: rotate(22deg); }
        50% { transform: rotate(0deg); }
        75% { transform: rotate(-22deg); }
        100% { filter: hue-rotate(360deg); }
    }

    .liquid {
        position: absolute;
        top: 50%;
        left: 5px;
        right: 5px;
        bottom: 5px;
        background: #1ae907;
        border-bottom-left-radius: 150px;
        border-bottom-right-radius: 150px;
        filter: drop-shadow(0 0 80px #1ae907);
        transform-origin: top center;
        animation: animateliquid 5s linear infinite;
    }

    @keyframes animateliquid {
        0%   { transform: rotate(0deg); }
        25%  { transform: rotate(-22deg); }
        30%  { transform: rotate(-23deg); }
        50%  { transform: rotate(0deg); }
        75%  { transform: rotate(22deg); }
        100% { transform: rotate(0deg); }
    }

    /* surface of the liquid */
    .liquid::before {
        content: '';
        position: absolute;
        top: -10px;
        width: 100%;
        height: 20px;
        background: #15be05;
        border-radius: 50%;
        filter: drop-shadow(0 0 80px #15be05);
    }

        /* same color change to text as liquid */
    .liquid-text {
        color: #1ae907;
        text-shadow: 0 0 24px currentColor;
        animation: textHue 5s linear infinite;
    }
    /* inverses the text color to pop out more cause I like it better */
    .liquid-text-inverse {
    animation-delay: -2.5s;
    }

    @keyframes textHue {
        from { filter: hue-rotate(0deg); }
        to   { filter: hue-rotate(360deg); }
    }

</style>