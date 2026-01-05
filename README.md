<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🚗 Divine Karnataka Road Trip | 7-Day Sacred Journey</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700;900&family=Poppins:wght@300;400;500;600;700&family=Caveat:wght@400;700&family=Satisfy&display=swap" rel="stylesheet">
    <style>
        :root {
            --road-black: #1a1a2e;
            --asphalt: #16213e;
            --sunset-orange: #ff6b35;
            --sunrise-gold: #f7c873;
            --ocean-deep: #0077b6;
            --ocean-light: #00b4d8;
            --ocean-foam: #caf0f8;
            --sand-light: #f4e4ba;
            --sand-dark: #d4a373;
            --temple-saffron: #ff6b00;
            --temple-gold: #ffd700;
            --forest-green: #2d6a4f;
            --coffee-brown: #6f4e37;
            --sky-blue: #87ceeb;
            --cloud-white: #f8f9fa;
            --coconut-green: #228b22;
            --coral: #ff7f50;
            --pearl: #fdeef4;
            --lighthouse-red: #dc2f02;
            --mountain-purple: #7b2cbf;
            --mist-gray: #adb5bd;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(180deg,
                #0a0a1a 0%,
                #1a1a3e 20%,
                #0d2137 40%,
                #0a2540 60%,
                #0d3b4d 80%,
                #1a4a5e 100%
            );
            color: #fff;
            overflow-x: hidden;
            min-height: 100vh;
        }

        /* ==================== SKY LAYER ==================== */
        .sky-layer {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            overflow: hidden;
        }

        /* Sun */
        .sun {
            position: absolute;
            top: 80px;
            right: 10%;
            width: 120px;
            height: 120px;
            background: radial-gradient(circle, #fff700 0%, #ff8c00 50%, #ff4500 100%);
            border-radius: 50%;
            box-shadow:
                0 0 60px #ff8c00,
                0 0 100px #ff6b00,
                0 0 150px #ff4500,
                0 0 200px rgba(255, 107, 0, 0.5);
            animation: sunPulse 4s ease-in-out infinite;
        }

        .sun::before {
            content: '';
            position: absolute;
            top: -20px;
            left: -20px;
            right: -20px;
            bottom: -20px;
            background: radial-gradient(circle, rgba(255, 200, 0, 0.3) 0%, transparent 70%);
            animation: sunRays 3s linear infinite;
        }

        @keyframes sunPulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        @keyframes sunRays {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Clouds */
        .cloud {
            position: absolute;
            background: linear-gradient(180deg, #fff 0%, #f0f0f0 100%);
            border-radius: 100px;
            opacity: 0.8;
            animation: cloudFloat linear infinite;
        }

        .cloud::before, .cloud::after {
            content: '';
            position: absolute;
            background: inherit;
            border-radius: 50%;
        }

        .cloud-1 {
            width: 150px;
            height: 50px;
            top: 50px;
            left: -150px;
            animation-duration: 45s;
        }
        .cloud-1::before { width: 70px; height: 70px; top: -35px; left: 20px; }
        .cloud-1::after { width: 50px; height: 50px; top: -25px; left: 70px; }

        .cloud-2 {
            width: 200px;
            height: 60px;
            top: 120px;
            left: -200px;
            animation-duration: 60s;
            animation-delay: -20s;
        }
        .cloud-2::before { width: 90px; height: 90px; top: -45px; left: 30px; }
        .cloud-2::after { width: 70px; height: 70px; top: -35px; left: 100px; }

        .cloud-3 {
            width: 120px;
            height: 40px;
            top: 180px;
            left: -120px;
            animation-duration: 50s;
            animation-delay: -35s;
        }
        .cloud-3::before { width: 50px; height: 50px; top: -25px; left: 15px; }
        .cloud-3::after { width: 40px; height: 40px; top: -20px; left: 55px; }

        @keyframes cloudFloat {
            0% { transform: translateX(0); }
            100% { transform: translateX(calc(100vw + 300px)); }
        }

        /* Birds */
        .bird {
            position: absolute;
            font-size: 1.5rem;
            opacity: 0.7;
            animation: birdFly linear infinite;
        }

        .bird-1 { top: 100px; animation-duration: 15s; animation-delay: 0s; }
        .bird-2 { top: 150px; animation-duration: 18s; animation-delay: -5s; }
        .bird-3 { top: 80px; animation-duration: 20s; animation-delay: -10s; }
        .bird-4 { top: 200px; animation-duration: 16s; animation-delay: -8s; }
        .bird-5 { top: 130px; animation-duration: 22s; animation-delay: -15s; }

        @keyframes birdFly {
            0% { left: -50px; transform: rotateY(0deg); }
            100% { left: 110%; transform: rotateY(0deg); }
        }

        /* ==================== OCEAN LAYER ==================== */
        .ocean-layer {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 300px;
            z-index: 1;
            overflow: hidden;
        }

        /* Ocean Gradient */
        .ocean-gradient {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(180deg,
                transparent 0%,
                rgba(0, 119, 182, 0.3) 20%,
                rgba(0, 180, 216, 0.5) 50%,
                rgba(0, 119, 182, 0.8) 80%,
                #005f8a 100%
            );
        }

        /* Waves */
        .wave {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 200%;
            height: 100px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cpath fill='%230099cc' fill-opacity='0.6' d='M0,160L48,170.7C96,181,192,203,288,192C384,181,480,139,576,138.7C672,139,768,181,864,197.3C960,213,1056,203,1152,176C1248,149,1344,107,1392,85.3L1440,64L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z'%3E%3C/path%3E%3C/svg%3E") repeat-x;
            background-size: 50% 100%;
            animation: waveMove 8s linear infinite;
        }

        .wave-2 {
            bottom: -10px;
            opacity: 0.7;
            animation: waveMove 10s linear infinite reverse;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cpath fill='%230077b6' fill-opacity='0.8' d='M0,224L48,213.3C96,203,192,181,288,181.3C384,181,480,203,576,218.7C672,235,768,245,864,234.7C960,224,1056,192,1152,181.3C1248,171,1344,181,1392,186.7L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z'%3E%3C/path%3E%3C/svg%3E") repeat-x;
            background-size: 50% 100%;
        }

        .wave-3 {
            bottom: -20px;
            opacity: 0.5;
            animation: waveMove 12s linear infinite;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cpath fill='%23023e8a' fill-opacity='0.9' d='M0,288L48,272C96,256,192,224,288,213.3C384,203,480,213,576,229.3C672,245,768,267,864,261.3C960,256,1056,224,1152,213.3C1248,203,1344,213,1392,218.7L1440,224L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z'%3E%3C/path%3E%3C/svg%3E") repeat-x;
            background-size: 50% 100%;
        }

        .wave-foam {
            bottom: 0;
            height: 60px;
            background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 320'%3E%3Cpath fill='%23caf0f8' fill-opacity='0.4' d='M0,256L48,261.3C96,267,192,277,288,266.7C384,256,480,224,576,213.3C672,203,768,213,864,229.3C960,245,1056,267,1152,261.3C1248,256,1344,224,1392,208L1440,192L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z'%3E%3C/path%3E%3C/svg%3E") repeat-x;
            background-size: 50% 100%;
            animation: waveMove 6s linear infinite;
        }

        @keyframes waveMove {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }

        /* Dolphins */
        .dolphin-container {
            position: absolute;
            bottom: 80px;
            animation: dolphinSwim 12s ease-in-out infinite;
        }

        .dolphin {
            font-size: 3rem;
            animation: dolphinJump 3s ease-in-out infinite;
            filter: drop-shadow(0 5px 15px rgba(0, 0, 0, 0.3));
        }

        .dolphin-1 { left: 20%; animation-delay: 0s; }
        .dolphin-2 { left: 50%; animation-delay: -4s; }
        .dolphin-3 { left: 75%; animation-delay: -8s; }

        @keyframes dolphinSwim {
            0%, 100% { transform: translateX(-100px); }
            50% { transform: translateX(100px); }
        }

        @keyframes dolphinJump {
            0%, 100% { transform: translateY(0) rotate(0deg); }
            25% { transform: translateY(-80px) rotate(-20deg); }
            50% { transform: translateY(0) rotate(0deg); }
            75% { transform: translateY(-60px) rotate(15deg); }
        }

        /* Fish */
        .fish {
            position: absolute;
            font-size: 1.5rem;
            animation: fishSwim linear infinite;
            opacity: 0.8;
        }

        .fish-1 { bottom: 40px; animation-duration: 20s; }
        .fish-2 { bottom: 60px; animation-duration: 25s; animation-delay: -10s; font-size: 1.2rem; }
        .fish-3 { bottom: 30px; animation-duration: 18s; animation-delay: -5s; font-size: 1.8rem; }
        .fish-4 { bottom: 50px; animation-duration: 22s; animation-delay: -15s; }
        .fish-5 { bottom: 70px; animation-duration: 28s; animation-delay: -8s; font-size: 1rem; }

        @keyframes fishSwim {
            0% { left: -50px; transform: scaleX(1); }
            49% { transform: scaleX(1); }
            50% { left: calc(100% + 50px); transform: scaleX(-1); }
            99% { transform: scaleX(-1); }
            100% { left: -50px; transform: scaleX(1); }
        }

        /* Boats and Ships */
        .boat {
            position: absolute;
            font-size: 3rem;
            animation: boatFloat ease-in-out infinite, boatMove linear infinite;
        }

        .boat-1 {
            bottom: 100px;
            font-size: 4rem;
            animation: boatFloat 4s ease-in-out infinite, boatMove 60s linear infinite;
        }

        .boat-2 {
            bottom: 130px;
            font-size: 2.5rem;
            animation: boatFloat 3s ease-in-out infinite, boatMove 80s linear infinite reverse;
            animation-delay: -20s;
        }

        .ship {
            position: absolute;
            bottom: 150px;
            font-size: 5rem;
            animation: boatFloat 5s ease-in-out infinite, shipMove 120s linear infinite;
            filter: drop-shadow(0 10px 30px rgba(0, 0, 0, 0.4));
        }

        @keyframes boatFloat {
            0%, 100% { transform: translateY(0) rotate(-2deg); }
            50% { transform: translateY(-15px) rotate(2deg); }
        }

        @keyframes boatMove {
            0% { left: -100px; }
            100% { left: calc(100% + 100px); }
        }

        @keyframes shipMove {
            0% { left: -150px; }
            100% { left: calc(100% + 150px); }
        }

        /* Lighthouse */
        .lighthouse {
            position: absolute;
            bottom: 80px;
            right: 8%;
            font-size: 5rem;
            filter: drop-shadow(0 5px 20px rgba(0, 0, 0, 0.5));
            animation: lighthouseGlow 2s ease-in-out infinite;
        }

        .lighthouse-beam {
            position: absolute;
            bottom: 130px;
            right: 10%;
            width: 300px;
            height: 4px;
            background: linear-gradient(90deg, rgba(255, 255, 0, 0.8), transparent);
            transform-origin: left center;
            animation: beamRotate 4s linear infinite;
            opacity: 0.6;
        }

        @keyframes lighthouseGlow {
            0%, 100% { filter: drop-shadow(0 5px 20px rgba(255, 255, 0, 0.3)); }
            50% { filter: drop-shadow(0 5px 40px rgba(255, 255, 0, 0.8)); }
        }

        @keyframes beamRotate {
            0% { transform: rotate(-30deg); opacity: 0.8; }
            50% { transform: rotate(30deg); opacity: 0.3; }
            100% { transform: rotate(-30deg); opacity: 0.8; }
        }

        /* ==================== BEACH & SAND LAYER ==================== */
        .beach-layer {
            position: fixed;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 80px;
            z-index: 2;
            background: linear-gradient(180deg,
                var(--sand-light) 0%,
                var(--sand-dark) 100%
            );
            overflow: hidden;
        }

        /* Sand Texture */
        .sand-texture {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image:
                radial-gradient(circle at 20% 30%, rgba(210, 180, 140, 0.5) 1px, transparent 1px),
                radial-gradient(circle at 60% 70%, rgba(210, 180, 140, 0.5) 1px, transparent 1px),
                radial-gradient(circle at 80% 20%, rgba(210, 180, 140, 0.5) 1px, transparent 1px);
            background-size: 20px 20px;
        }

        /* Seashells */
        .seashell {
            position: absolute;
            bottom: 10px;
            font-size: 1.5rem;
            animation: shellShine 3s ease-in-out infinite;
        }

        .shell-1 { left: 5%; font-size: 1.2rem; animation-delay: 0s; }
        .shell-2 { left: 15%; font-size: 1.8rem; animation-delay: -1s; }
        .shell-3 { left: 25%; font-size: 1rem; animation-delay: -2s; }
        .shell-4 { left: 40%; font-size: 1.5rem; animation-delay: -0.5s; }
        .shell-5 { left: 55%; font-size: 1.3rem; animation-delay: -1.5s; }
        .shell-6 { left: 70%; font-size: 1.7rem; animation-delay: -2.5s; }
        .shell-7 { left: 85%; font-size: 1.1rem; animation-delay: -0.8s; }
        .shell-8 { left: 92%; font-size: 1.4rem; animation-delay: -1.8s; }

        @keyframes shellShine {
            0%, 100% { filter: brightness(1) drop-shadow(0 2px 5px rgba(0,0,0,0.2)); }
            50% { filter: brightness(1.3) drop-shadow(0 2px 10px rgba(255,215,0,0.4)); }
        }

        /* Starfish */
        .starfish {
            position: absolute;
            font-size: 2rem;
            animation: starfishRotate 10s linear infinite;
        }

        .starfish-1 { left: 10%; bottom: 15px; animation-delay: 0s; }
        .starfish-2 { left: 45%; bottom: 20px; animation-delay: -3s; font-size: 1.5rem; }
        .starfish-3 { left: 78%; bottom: 12px; animation-delay: -6s; font-size: 1.8rem; }

        @keyframes starfishRotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Crabs */
        .crab {
            position: absolute;
            bottom: 25px;
            font-size: 1.8rem;
            animation: crabWalk 15s linear infinite;
        }

        .crab-1 { animation-duration: 20s; }
        .crab-2 { animation-duration: 25s; animation-delay: -10s; font-size: 1.5rem; }

        @keyframes crabWalk {
            0% { left: -50px; transform: scaleX(1); }
            49% { transform: scaleX(1); }
            50% { left: calc(100% + 50px); transform: scaleX(-1); }
            99% { transform: scaleX(-1); }
            100% { left: -50px; transform: scaleX(1); }
        }

        /* ==================== PALM TREES & VEGETATION ==================== */
        .vegetation-layer {
            position: fixed;
            bottom: 60px;
            left: 0;
            width: 100%;
            height: 200px;
            z-index: 3;
            pointer-events: none;
            overflow: hidden;
        }

        .palm-tree {
            position: absolute;
            bottom: 0;
            font-size: 6rem;
            filter: drop-shadow(2px 5px 10px rgba(0, 0, 0, 0.3));
            animation: palmSway 4s ease-in-out infinite;
            transform-origin: bottom center;
        }

        .palm-1 { left: 2%; font-size: 7rem; animation-delay: 0s; }
        .palm-2 { left: 8%; font-size: 5rem; animation-delay: -1s; }
        .palm-3 { right: 3%; font-size: 8rem; animation-delay: -2s; }
        .palm-4 { right: 12%; font-size: 5.5rem; animation-delay: -0.5s; }

        @keyframes palmSway {
            0%, 100% { transform: rotate(-3deg); }
            50% { transform: rotate(3deg); }
        }

        /* Coconuts falling occasionally */
        .coconut {
            position: absolute;
            font-size: 1.5rem;
            opacity: 0;
            animation: coconutFall 8s ease-in infinite;
        }

        .coconut-1 { left: 5%; animation-delay: 0s; }
        .coconut-2 { right: 8%; animation-delay: -4s; }

        @keyframes coconutFall {
            0% { top: 40%; opacity: 0; transform: rotate(0deg); }
            5% { opacity: 1; }
            50% { top: calc(100% - 100px); opacity: 1; transform: rotate(720deg); }
            51% { opacity: 0; }
            100% { opacity: 0; }
        }

        /* ==================== TEMPLES & LANDMARKS ==================== */
        .landmarks-layer {
            position: fixed;
            bottom: 100px;
            left: 0;
            width: 100%;
            height: 300px;
            z-index: 2;
            pointer-events: none;
            overflow: hidden;
        }

        .temple-silhouette {
            position: absolute;
            font-size: 4rem;
            opacity: 0.15;
            animation: templeShimmer 5s ease-in-out infinite;
        }

        .temple-1 { left: 20%; bottom: 50px; font-size: 5rem; animation-delay: 0s; }
        .temple-2 { left: 45%; bottom: 80px; font-size: 6rem; animation-delay: -2s; }
        .temple-3 { left: 70%; bottom: 40px; font-size: 4.5rem; animation-delay: -4s; }

        @keyframes templeShimmer {
            0%, 100% {
                opacity: 0.15;
                filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.2));
            }
            50% {
                opacity: 0.25;
                filter: drop-shadow(0 0 30px rgba(255, 215, 0, 0.5));
            }
        }

        /* Mountains in background */
        .mountain {
            position: absolute;
            bottom: 80px;
            width: 0;
            height: 0;
            opacity: 0.2;
        }

        .mountain-1 {
            left: 5%;
            border-left: 100px solid transparent;
            border-right: 100px solid transparent;
            border-bottom: 150px solid #4a5568;
        }

        .mountain-2 {
            left: 15%;
            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-bottom: 200px solid #2d3748;
        }

        .mountain-3 {
            right: 10%;
            border-left: 120px solid transparent;
            border-right: 120px solid transparent;
            border-bottom: 170px solid #4a5568;
        }

        /* ==================== ROAD ANIMATION ==================== */
        .road-layer {
            position: fixed;
            bottom: 70px;
            left: 0;
            width: 100%;
            height: 40px;
            z-index: 4;
            background: linear-gradient(180deg, #333 0%, #1a1a1a 100%);
            overflow: hidden;
        }

        .road-marking {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            height: 4px;
            width: 60px;
            background: #fff;
            animation: roadMarkingMove 1s linear infinite;
        }

        .marking-1 { left: 0%; animation-delay: 0s; }
        .marking-2 { left: 15%; animation-delay: -0.15s; }
        .marking-3 { left: 30%; animation-delay: -0.3s; }
        .marking-4 { left: 45%; animation-delay: -0.45s; }
        .marking-5 { left: 60%; animation-delay: -0.6s; }
        .marking-6 { left: 75%; animation-delay: -0.75s; }
        .marking-7 { left: 90%; animation-delay: -0.9s; }

        @keyframes roadMarkingMove {
            0% { transform: translateY(-50%) translateX(0); }
            100% { transform: translateY(-50%) translateX(-150px); }
        }

        /* Car on road */
        .car-container {
            position: fixed;
            bottom: 75px;
            z-index: 5;
            animation: carDrive 20s linear infinite;
        }

        .car {
            font-size: 3rem;
            filter: drop-shadow(0 5px 15px rgba(0, 0, 0, 0.5));
            animation: carBounce 0.5s ease-in-out infinite;
        }

        @keyframes carDrive {
            0% { left: -100px; }
            100% { left: calc(100% + 100px); }
        }

        @keyframes carBounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-3px); }
        }

        /* Milestones */
        .milestone {
            position: fixed;
            bottom: 110px;
            z-index: 4;
            font-size: 0.8rem;
            background: linear-gradient(135deg, #fff 0%, #e0e0e0 100%);
            color: #333;
            padding: 5px 10px;
            border-radius: 3px;
            font-weight: 600;
            animation: milestonePass 15s linear infinite;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.3);
        }

        .milestone::before {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 15px;
            background: #888;
        }

        .milestone-1 { animation-delay: 0s; }
        .milestone-2 { animation-delay: -5s; }
        .milestone-3 { animation-delay: -10s; }

        @keyframes milestonePass {
            0% { right: -100px; opacity: 0; }
            5% { opacity: 1; }
            95% { opacity: 1; }
            100% { right: calc(100% + 100px); opacity: 0; }
        }

        /* ==================== FLOATING ELEMENTS ==================== */
        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 6;
            overflow: hidden;
        }

        /* Diyas (Lamps) */
        .diya {
            position: absolute;
            font-size: 2rem;
            animation: diyaFloat ease-in-out infinite;
            filter: drop-shadow(0 0 15px rgba(255, 165, 0, 0.8));
        }

        .diya-1 { left: 5%; top: 20%; animation-duration: 6s; }
        .diya-2 { right: 8%; top: 35%; animation-duration: 7s; animation-delay: -2s; }
        .diya-3 { left: 15%; top: 50%; animation-duration: 5s; animation-delay: -4s; }
        .diya-4 { right: 15%; top: 15%; animation-duration: 8s; animation-delay: -1s; }

        @keyframes diyaFloat {
            0%, 100% {
                transform: translateY(0) scale(1);
                filter: drop-shadow(0 0 15px rgba(255, 165, 0, 0.6));
            }
            50% {
                transform: translateY(-20px) scale(1.1);
                filter: drop-shadow(0 0 30px rgba(255, 165, 0, 1));
            }
        }

        /* Food Elements */
        .food-float {
            position: absolute;
            font-size: 2.5rem;
            opacity: 0;
            animation: foodFloat 20s ease-in-out infinite;
        }

        .food-1 { left: 10%; animation-delay: 0s; }
        .food-2 { left: 30%; animation-delay: -5s; }
        .food-3 { left: 50%; animation-delay: -10s; }
        .food-4 { left: 70%; animation-delay: -15s; }
        .food-5 { left: 85%; animation-delay: -3s; }

        @keyframes foodFloat {
            0% { top: 100%; opacity: 0; transform: rotate(0deg) scale(0.5); }
            10% { opacity: 0.8; transform: scale(1); }
            90% { opacity: 0.8; }
            100% { top: -100px; opacity: 0; transform: rotate(360deg) scale(0.5); }
        }

        /* Flowers */
        .flower {
            position: absolute;
            font-size: 2rem;
            animation: flowerDrift linear infinite;
            opacity: 0.8;
        }

        .flower-1 { animation-duration: 15s; animation-delay: 0s; }
        .flower-2 { animation-duration: 18s; animation-delay: -3s; }
        .flower-3 { animation-duration: 20s; animation-delay: -7s; }
        .flower-4 { animation-duration: 16s; animation-delay: -11s; }
        .flower-5 { animation-duration: 22s; animation-delay: -5s; }

        @keyframes flowerDrift {
            0% {
                top: -50px;
                left: var(--start-pos);
                transform: rotate(0deg);
            }
            25% { left: calc(var(--start-pos) + 50px); }
            50% { left: calc(var(--start-pos) - 30px); }
            75% { left: calc(var(--start-pos) + 30px); }
            100% {
                top: 100vh;
                left: var(--start-pos);
                transform: rotate(720deg);
            }
        }

        .flower-1 { --start-pos: 10%; }
        .flower-2 { --start-pos: 25%; }
        .flower-3 { --start-pos: 50%; }
        .flower-4 { --start-pos: 70%; }
        .flower-5 { --start-pos: 90%; }

        /* ==================== MAIN CONTENT ==================== */
        .main-content {
            position: relative;
            z-index: 100;
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
            padding-bottom: 350px;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 40px 20px;
            position: relative;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 10px 25px;
            background: rgba(255, 107, 0, 0.2);
            border: 1px solid var(--sunset-orange);
            border-radius: 50px;
            font-size: 0.9rem;
            color: var(--sunrise-gold);
            margin-bottom: 20px;
            animation: badgePulse 2s ease-in-out infinite;
        }

        @keyframes badgePulse {
            0%, 100% { box-shadow: 0 0 20px rgba(255, 107, 0, 0.3); }
            50% { box-shadow: 0 0 40px rgba(255, 107, 0, 0.6); }
        }

        .hero-icon {
            font-size: 6rem;
            margin-bottom: 20px;
            animation: heroIconBounce 3s ease-in-out infinite;
            filter: drop-shadow(0 10px 30px rgba(255, 107, 0, 0.5));
        }

        @keyframes heroIconBounce {
            0%, 100% { transform: translateY(0) rotate(-5deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }

        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2.5rem, 7vw, 5rem);
            font-weight: 900;
            background: linear-gradient(135deg,
                var(--sunrise-gold) 0%,
                #fff 25%,
                var(--sunset-orange) 50%,
                var(--sunrise-gold) 75%,
                #fff 100%
            );
            background-size: 200% auto;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: textShimmer 4s linear infinite;
            margin-bottom: 15px;
            line-height: 1.2;
        }

        @keyframes textShimmer {
            0% { background-position: 0% center; }
            100% { background-position: 200% center; }
        }

        .hero-subtitle {
            font-family: 'Caveat', cursive;
            font-size: clamp(1.5rem, 4vw, 2.5rem);
            color: var(--ocean-light);
            margin-bottom: 30px;
        }

        .hero-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin: 30px 0;
        }

        .stat-item {
            text-align: center;
            padding: 20px 30px;
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            border: 1px solid rgba(255, 215, 0, 0.2);
            min-width: 120px;
            transition: all 0.3s ease;
        }

        .stat-item:hover {
            transform: translateY(-10px);
            background: rgba(255, 215, 0, 0.1);
            border-color: rgba(255, 215, 0, 0.5);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(135deg, var(--temple-gold), var(--sunset-orange));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .stat-label {
            font-size: 0.85rem;
            color: var(--sand-light);
            margin-top: 5px;
        }

        /* Route Preview */
        .route-preview {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            gap: 15px;
            padding: 30px;
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(15px);
            border-radius: 30px;
            margin: 40px 0;
            border: 1px solid rgba(255, 215, 0, 0.2);
        }

        .route-stop {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            background: linear-gradient(135deg, rgba(255, 107, 0, 0.2), rgba(255, 215, 0, 0.1));
            border-radius: 25px;
            font-size: 0.9rem;
            border: 1px solid rgba(255, 215, 0, 0.3);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .route-stop:hover {
            transform: scale(1.1) translateY(-5px);
            background: linear-gradient(135deg, rgba(255, 107, 0, 0.4), rgba(255, 215, 0, 0.3));
            box-shadow: 0 15px 40px rgba(255, 215, 0, 0.3);
        }

        .route-arrow {
            font-size: 1.5rem;
            color: var(--temple-gold);
            animation: arrowPulse 1.5s ease-in-out infinite;
        }

        @keyframes arrowPulse {
            0%, 100% { opacity: 0.5; transform: translateX(0); }
            50% { opacity: 1; transform: translateX(5px); }
        }

        /* Scroll Indicator */
        .scroll-indicator {
            position: absolute;
            bottom: 80px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            animation: scrollBounce 2s ease-in-out infinite;
        }

        .scroll-text {
            font-size: 0.8rem;
            letter-spacing: 3px;
            color: var(--sand-light);
            text-transform: uppercase;
        }

        .scroll-mouse {
            width: 30px;
            height: 50px;
            border: 2px solid var(--temple-gold);
            border-radius: 25px;
            position: relative;
        }

        .scroll-mouse::before {
            content: '';
            position: absolute;
            top: 8px;
            left: 50%;
            transform: translateX(-50%);
            width: 4px;
            height: 10px;
            background: var(--temple-gold);
            border-radius: 2px;
            animation: mouseScroll 2s infinite;
        }

        @keyframes scrollBounce {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(15px); }
        }

        @keyframes mouseScroll {
            0% { top: 8px; opacity: 1; }
            100% { top: 30px; opacity: 0; }
        }

        /* ==================== DAY SECTIONS ==================== */
        .day-section {
            margin: 80px 0;
            position: relative;
        }

        .section-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-emoji {
            font-size: 4rem;
            margin-bottom: 15px;
            animation: emojiFloat 3s ease-in-out infinite;
        }

        @keyframes emojiFloat {
            0%, 100% { transform: translateY(0) rotate(-5deg); }
            50% { transform: translateY(-15px) rotate(5deg); }
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: clamp(2rem, 5vw, 3.5rem);
            background: linear-gradient(135deg, var(--temple-gold), #fff, var(--sunset-orange));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 10px;
        }

        .section-subtitle {
            font-size: 1.1rem;
            color: var(--ocean-light);
        }

        .decorative-line {
            width: 200px;
            height: 4px;
            margin: 25px auto;
            background: linear-gradient(90deg, transparent, var(--temple-gold), var(--sunset-orange), var(--temple-gold), transparent);
            position: relative;
            border-radius: 2px;
        }

        .decorative-line::before {
            content: '◆';
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            font-size: 1rem;
            color: var(--temple-gold);
            background: var(--road-black);
            padding: 0 15px;
        }

        /* Day Card */
        .day-card {
            background: linear-gradient(135deg, rgba(255, 255, 255, 0.08), rgba(255, 255, 255, 0.02));
            backdrop-filter: blur(20px);
            border-radius: 30px;
            padding: 40px;
            margin: 30px 0;
            border: 1px solid rgba(255, 215, 0, 0.15);
            position: relative;
            overflow: hidden;
            transition: all 0.5s ease;
        }

        .day-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, var(--sunset-orange), var(--temple-gold), var(--sunrise-gold), var(--temple-gold), var(--sunset-orange));
        }

        .day-card::after {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255, 215, 0, 0.05) 0%, transparent 50%);
            animation: cardGlow 15s linear infinite;
            pointer-events: none;
        }

        @keyframes cardGlow {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .day-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 40px 80px rgba(255, 107, 0, 0.2);
            border-color: rgba(255, 215, 0, 0.4);
        }

        .day-header {
            display: flex;
            align-items: center;
            gap: 25px;
            margin-bottom: 30px;
            flex-wrap: wrap;
            position: relative;
            z-index: 1;
        }

        .day-badge {
            width: 90px;
            height: 90px;
            background: linear-gradient(135deg, var(--sunset-orange), var(--temple-gold));
            border-radius: 50%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: #000;
            box-shadow: 0 15px 40px rgba(255, 107, 0, 0.4);
            flex-shrink: 0;
        }

        .day-badge span:first-child {
            font-size: 0.7rem;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .day-badge span:last-child {
            font-size: 2rem;
        }

        .day-info {
            flex: 1;
        }

        .day-info h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            color: var(--temple-gold);
            margin-bottom: 8px;
        }

        .day-info p {
            color: var(--sand-light);
            font-size: 1rem;
        }

        .day-tag {
            padding: 8px 20px;
            border-radius: 25px;
            font-size: 0.85rem;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .tag-coastal {
            background: rgba(0, 180, 216, 0.2);
            color: var(--ocean-light);
            border: 1px solid rgba(0, 180, 216, 0.4);
        }

        .tag-temple {
            background: rgba(255, 107, 0, 0.2);
            color: var(--sunset-orange);
            border: 1px solid rgba(255, 107, 0, 0.4);
        }

        .tag-mountain {
            background: rgba(45, 106, 79, 0.2);
            color: #90EE90;
            border: 1px solid rgba(45, 106, 79, 0.4);
        }

        .tag-heritage {
            background: rgba(139, 69, 19, 0.2);
            color: var(--sand-dark);
            border: 1px solid rgba(139, 69, 19, 0.4);
        }

        .tag-return {
            background: rgba(255, 215, 0, 0.2);
            color: var(--temple-gold);
            border: 1px solid rgba(255, 215, 0, 0.4);
        }

        /* Info Grid */
        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin: 30px 0;
            position: relative;
            z-index: 1;
        }

        .info-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            border: 1px solid rgba(255, 215, 0, 0.1);
            transition: all 0.3s ease;
        }

        .info-item:hover {
            background: rgba(255, 215, 0, 0.1);
            transform: translateY(-5px);
        }

        .info-icon {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .info-label {
            font-size: 0.75rem;
            color: #888;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 5px;
        }

        .info-value {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--temple-gold);
        }

        /* Route Box */
        .route-box {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.1));
            border-radius: 20px;
            padding: 25px;
            margin: 25px 0;
            border-left: 5px solid var(--sunset-orange);
            position: relative;
            z-index: 1;
        }

        .route-box h4 {
            color: var(--temple-gold);
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .route-path {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 10px;
            font-size: 0.95rem;
            color: #ccc;
        }

        .route-path span {
            padding: 8px 15px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            transition: all 0.3s ease;
        }

        .route-path span:hover {
            background: rgba(255, 107, 0, 0.2);
            color: var(--sunset-orange);
        }

        .route-path .arrow {
            color: var(--temple-gold);
            background: transparent;
        }

        /* Timeline */
        .timeline {
            position: relative;
            margin: 40px 0;
            padding-left: 60px;
        }

        .timeline::before {
            content: '';
            position: absolute;
            left: 25px;
            top: 0;
            bottom: 0;
            width: 4px;
            background: linear-gradient(180deg, var(--sunset-orange), var(--temple-gold), var(--ocean-light), var(--temple-gold), var(--sunset-orange));
            border-radius: 2px;
        }

        .timeline-item {
            position: relative;
            margin-bottom: 30px;
            padding: 25px;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 20px;
            border: 1px solid rgba(255, 215, 0, 0.1);
            transition: all 0.3s ease;
        }

        .timeline-item::before {
            content: '';
            position: absolute;
            left: -43px;
            top: 30px;
            width: 20px;
            height: 20px;
            background: linear-gradient(135deg, var(--sunset-orange), var(--temple-gold));
            border-radius: 50%;
            box-shadow: 0 0 20px rgba(255, 215, 0, 0.5);
            z-index: 1;
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            left: -35px;
            top: 38px;
            width: 4px;
            height: 4px;
            background: #fff;
            border-radius: 50%;
        }

        .timeline-item:hover {
            background: rgba(255, 215, 0, 0.05);
            transform: translateX(10px);
            border-color: rgba(255, 215, 0, 0.3);
        }

        .timeline-time {
            font-size: 1.1rem;
            font-weight: 700;
            color: var(--temple-gold);
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .timeline-content h4 {
            font-size: 1.2rem;
            margin-bottom: 8px;
            color: #fff;
        }

        .timeline-content p {
            color: #aaa;
            font-size: 0.95rem;
            line-height: 1.6;
        }

        /* Temple Cards */
        .temples-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }

        .temple-card {
            background: linear-gradient(135deg, rgba(139, 69, 19, 0.2), rgba(255, 107, 0, 0.1));
            border-radius: 25px;
            padding: 30px;
            border: 2px solid rgba(255, 215, 0, 0.2);
            position: relative;
            overflow: hidden;
            transition: all 0.4s ease;
        }

        .temple-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--sunset-orange), var(--temple-gold), var(--sunset-orange));
        }

        .temple-card::after {
            content: '🕉️';
            position: absolute;
            top: 15px;
            right: 15px;
            font-size: 2rem;
            opacity: 0.2;
        }

        .temple-card:hover {
            transform: translateY(-10px) scale(1.02);
            box-shadow: 0 25px 60px rgba(255, 107, 0, 0.3);
            border-color: rgba(255, 215, 0, 0.5);
        }

        .temple-card h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: var(--temple-gold);
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .temple-card .deity {
            font-size: 0.9rem;
            color: var(--sand-light);
            margin-bottom: 15px;
        }

        .temple-features {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 15px;
        }

        .temple-feature {
            padding: 5px 12px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            font-size: 0.8rem;
            color: #ccc;
        }

        /* Hotel Cards */
        .hotels-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
            margin: 30px 0;
        }

        .hotel-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 25px;
            padding: 25px;
            border: 1px solid rgba(255, 215, 0, 0.15);
            transition: all 0.3s ease;
            position: relative;
        }

        .hotel-card.recommended {
            border: 2px solid var(--temple-gold);
        }

        .hotel-card.recommended::before {
            content: '⭐ RECOMMENDED';
            position: absolute;
            top: -10px;
            left: 20px;
            background: linear-gradient(90deg, var(--temple-gold), var(--sunset-orange));
            color: #000;
            padding: 5px 15px;
            border-radius: 15px;
            font-size: 0.7rem;
            font-weight: 700;
        }

        .hotel-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 215, 0, 0.08);
        }

        .hotel-card h4 {
            color: var(--temple-gold);
            margin-bottom: 15px;
            font-size: 1.2rem;
        }

        .hotel-detail {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 10px;
            color: #ccc;
            font-size: 0.9rem;
        }

        .hotel-price {
            font-size: 1.4rem;
            font-weight: 700;
            color: #90EE90;
            margin-top: 15px;
        }

        /* Food Section */
        .food-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .food-item {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 25px;
            text-align: center;
            border: 1px solid rgba(76, 175, 80, 0.2);
            transition: all 0.3s ease;
        }

        .food-item:hover {
            transform: translateY(-10px) rotate(3deg);
            background: rgba(76, 175, 80, 0.1);
            border-color: rgba(76, 175, 80, 0.5);
        }

        .food-emoji {
            font-size: 3.5rem;
            margin-bottom: 15px;
            animation: foodBounce 2s ease-in-out infinite;
        }

        @keyframes foodBounce {
            0%, 100% { transform: translateY(0) scale(1); }
            50% { transform: translateY(-10px) scale(1.1); }
        }

        .food-item h5 {
            color: var(--temple-gold);
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .food-item p {
            color: #aaa;
            font-size: 0.85rem;
        }

        /* Highlights Box */
        .highlights-box {
            background: linear-gradient(135deg, rgba(255, 215, 0, 0.1), rgba(255, 107, 0, 0.05));
            border-left: 5px solid var(--temple-gold);
            padding: 25px;
            border-radius: 0 20px 20px 0;
            margin: 30px 0;
        }

        .highlights-box h4 {
            color: var(--temple-gold);
            margin-bottom: 15px;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .highlights-list {
            list-style: none;
        }

        .highlights-list li {
            padding: 10px 0;
            color: #ccc;
            display: flex;
            align-items: flex-start;
            gap: 12px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
        }

        .highlights-list li:last-child {
            border-bottom: none;
        }

        .highlights-list li::before {
            content: '✨';
            flex-shrink: 0;
        }

        /* Photo Spots */
        .photo-spots {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            margin: 20px 0;
        }

        .photo-spot {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 18px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 25px;
            font-size: 0.9rem;
            color: #ccc;
            border: 1px solid rgba(255, 107, 0, 0.2);
            transition: all 0.3s ease;
        }

        .photo-spot:hover {
            background: rgba(255, 107, 0, 0.2);
            color: var(--sunset-orange);
            transform: scale(1.05);
        }

        /* Tips Section */
        .tips-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .tip-card {
            background: rgba(255, 255, 255, 0.03);
            border-radius: 20px;
            padding: 25px;
            border-left: 4px solid var(--sunset-orange);
            display: flex;
            gap: 15px;
            transition: all 0.3s ease;
        }

        .tip-card:hover {
            background: rgba(255, 107, 0, 0.1);
            transform: translateX(10px);
        }

        .tip-number {
            width: 40px;
            height: 40px;
            background: linear-gradient(135deg, var(--sunset-orange), var(--temple-gold));
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 700;
            color: #000;
            flex-shrink: 0;
        }

        .tip-content h5 {
            color: var(--temple-gold);
            margin-bottom: 5px;
        }

        .tip-content p {
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Contacts Grid */
        .contacts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin: 30px 0;
        }

        .contact-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
            border: 1px solid rgba(255, 215, 0, 0.1);
            transition: all 0.3s ease;
        }

        .contact-card:hover {
            background: rgba(255, 215, 0, 0.1);
            transform: translateY(-5px);
        }

        .contact-icon {
            font-size: 2rem;
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 107, 0, 0.2);
            border-radius: 15px;
        }

        .contact-info strong {
            color: var(--temple-gold);
            display: block;
            margin-bottom: 3px;
        }

        .contact-info span {
            color: #aaa;
            font-size: 0.9rem;
        }

        /* Dividers */
        .section-divider {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 30px;
            margin: 80px 0;
        }

        .section-divider::before,
        .section-divider::after {
            content: '';
            flex: 1;
            max-width: 200px;
            height: 2px;
            background: linear-gradient(90deg, transparent, rgba(255, 215, 0, 0.5), transparent);
        }

        .divider-icons {
            display: flex;
            gap: 20px;
            font-size: 2rem;
            animation: dividerFloat 3s ease-in-out infinite;
        }

        @keyframes dividerFloat {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        /* Summary Table */
        .summary-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0 12px;
            margin: 30px 0;
        }

        .summary-table th {
            background: linear-gradient(135deg, rgba(255, 107, 0, 0.3), rgba(255, 215, 0, 0.2));
            color: var(--temple-gold);
            padding: 18px 20px;
            text-align: left;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.85rem;
        }

        .summary-table th:first-child {
            border-radius: 15px 0 0 15px;
        }

        .summary-table th:last-child {
            border-radius: 0 15px 15px 0;
        }

        .summary-table td {
            background: rgba(255, 255, 255, 0.03);
            padding: 18px 20px;
            color: #ccc;
            border-top: 1px solid rgba(255, 215, 0, 0.1);
            border-bottom: 1px solid rgba(255, 215, 0, 0.1);
            transition: all 0.3s ease;
        }

        .summary-table td:first-child {
            border-left: 1px solid rgba(255, 215, 0, 0.1);
            border-radius: 15px 0 0 15px;
        }

        .summary-table td:last-child {
            border-right: 1px solid rgba(255, 215, 0, 0.1);
            border-radius: 0 15px 15px 0;
        }

        .summary-table tr:hover td {
            background: rgba(255, 215, 0, 0.08);
        }

        /* Footer */
        .footer {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.3));
            padding: 60px 20px;
            text-align: center;
            margin-top: 80px;
            border-top: 1px solid rgba(255, 215, 0, 0.2);
            position: relative;
        }

        .footer::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg,
                var(--ocean-deep),
                var(--sunset-orange),
                var(--temple-gold),
                var(--forest-green),
                var(--temple-gold),
                var(--sunset-orange),
                var(--ocean-deep)
            );
        }

        .footer-emoji {
            font-size: 4rem;
            margin-bottom: 20px;
            animation: footerFloat 3s ease-in-out infinite;
        }

        @keyframes footerFloat {
            0%, 100% { transform: translateY(0) rotate(-5deg); }
            50% { transform: translateY(-15px) rotate(5deg); }
        }

        .footer-text {
            font-family: 'Caveat', cursive;
            font-size: 2rem;
            color: var(--temple-gold);
            margin-bottom: 15px;
        }

        .footer-subtext {
            color: var(--sand-light);
            font-size: 1rem;
            margin-bottom: 25px;
        }

        .footer-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            color: #888;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2rem;
            }

            .hero-icon {
                font-size: 4rem;
            }

            .day-card {
                padding: 25px;
            }

            .timeline {
                padding-left: 45px;
            }

            .timeline::before {
                left: 15px;
            }

            .timeline-item::before {
                left: -38px;
            }

            .sun {
                width: 80px;
                height: 80px;
                top: 50px;
            }

            .palm-tree {
                font-size: 4rem !important;
            }

            .ocean-layer {
                height: 200px;
            }
        }

        /* Scroll Animations */
        .reveal {
            opacity: 0;
            transform: translateY(60px);
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Cursor Trail Effect */
        .cursor-trail {
            position: fixed;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            pointer-events: none;
            z-index: 9999;
            mix-blend-mode: screen;
            animation: cursorFade 1s forwards;
        }

        @keyframes cursorFade {
            0% { transform: scale(1); opacity: 0.8; }
            100% { transform: scale(0); opacity: 0; }
        }
    </style>
</head>
<body>
    <!-- SKY LAYER -->
    <div class="sky-layer">
        <!-- Sun -->
        <div class="sun"></div>
       
        <!-- Clouds -->
        <div class="cloud cloud-1"></div>
        <div class="cloud cloud-2"></div>
        <div class="cloud cloud-3"></div>
       
        <!-- Birds -->
        <div class="bird bird-1">🐦</div>
        <div class="bird bird-2">🕊️</div>
        <div class="bird bird-3">🐦</div>
        <div class="bird bird-4">🕊️</div>
        <div class="bird bird-5">🐦</div>
    </div>

    <!-- LANDMARKS LAYER -->
    <div class="landmarks-layer">
        <div class="mountain mountain-1"></div>
        <div class="mountain mountain-2"></div>
        <div class="mountain mountain-3"></div>
        <div class="temple-silhouette temple-1">🛕</div>
        <div class="temple-silhouette temple-2">🕌</div>
        <div class="temple-silhouette temple-3">⛩️</div>
    </div>

    <!-- OCEAN LAYER -->
    <div class="ocean-layer">
        <div class="ocean-gradient"></div>
       
        <!-- Dolphins -->
        <div class="dolphin-container dolphin-1">
            <div class="dolphin">🐬</div>
        </div>
        <div class="dolphin-container dolphin-2">
            <div class="dolphin">🐬</div>
        </div>
        <div class="dolphin-container dolphin-3">
            <div class="dolphin">🐬</div>
        </div>
       
        <!-- Fish -->
        <div class="fish fish-1">🐠</div>
        <div class="fish fish-2">🐟</div>
        <div class="fish fish-3">🐡</div>
        <div class="fish fish-4">🐠</div>
        <div class="fish fish-5">🐟</div>
       
        <!-- Boats -->
        <div class="boat boat-1">⛵</div>
        <div class="boat boat-2">🚤</div>
        <div class="ship">🚢</div>
       
        <!-- Lighthouse -->
        <div class="lighthouse">🏠</div>
        <div class="lighthouse-beam"></div>
       
        <!-- Waves -->
        <div class="wave"></div>
        <div class="wave wave-2"></div>
        <div class="wave wave-3"></div>
        <div class="wave wave-foam"></div>
    </div>

    <!-- VEGETATION LAYER -->
    <div class="vegetation-layer">
        <div class="palm-tree palm-1">🌴</div>
        <div class="palm-tree palm-2">🌴</div>
        <div class="palm-tree palm-3">🌴</div>
        <div class="palm-tree palm-4">🌴</div>
        <div class="coconut coconut-1">🥥</div>
        <div class="coconut coconut-2">🥥</div>
    </div>

    <!-- BEACH LAYER -->
    <div class="beach-layer">
        <div class="sand-texture"></div>
       
        <!-- Seashells -->
        <div class="seashell shell-1">🐚</div>
        <div class="seashell shell-2">🐚</div>
        <div class="seashell shell-3">🦪</div>
        <div class="seashell shell-4">🐚</div>
        <div class="seashell shell-5">🦪</div>
        <div class="seashell shell-6">🐚</div>
        <div class="seashell shell-7">🦪</div>
        <div class="seashell shell-8">🐚</div>
       
        <!-- Starfish -->
        <div class="starfish starfish-1">⭐</div>
        <div class="starfish starfish-2">🌟</div>
        <div class="starfish starfish-3">⭐</div>
       
        <!-- Crabs -->
        <div class="crab crab-1">🦀</div>
        <div class="crab crab-2">🦀</div>
    </div>

    <!-- ROAD LAYER -->
    <div class="road-layer">
        <div class="road-marking marking-1"></div>
        <div class="road-marking marking-2"></div>
        <div class="road-marking marking-3"></div>
        <div class="road-marking marking-4"></div>
        <div class="road-marking marking-5"></div>
        <div class="road-marking marking-6"></div>
        <div class="road-marking marking-7"></div>
    </div>

    <!-- Car Animation -->
    <div class="car-container">
        <div class="car">🚗</div>
    </div>

    <!-- Milestones -->
    <div class="milestone milestone-1">Goa 150km</div>
    <div class="milestone milestone-2">Gokarna 280km</div>
    <div class="milestone milestone-3">Murdeshwar 320km</div>

    <!-- FLOATING ELEMENTS -->
    <div class="floating-elements">
        <!-- Diyas -->
        <div class="diya diya-1">🪔</div>
        <div class="diya diya-2">🪔</div>
        <div class="diya diya-3">🪔</div>
        <div class="diya diya-4">🪔</div>
       
        <!-- Food floating up -->
        <div class="food-float food-1">🥘</div>
        <div class="food-float food-2">🍛</div>
        <div class="food-float food-3">☕</div>
        <div class="food-float food-4">🫓</div>
        <div class="food-float food-5">🍚</div>
       
        <!-- Flowers -->
        <div class="flower flower-1">🌸</div>
        <div class="flower flower-2">🌺</div>
        <div class="flower flower-3">🌼</div>
        <div class="flower flower-4">🪷</div>
        <div class="flower flower-5">🌻</div>
    </div>

    <!-- MAIN CONTENT -->
    <div class="main-content">
        <!-- Hero Section -->
        <section class="hero">
            <div class="hero-badge">
                <span>🗓️</span>
                <span>7 DAYS • 1890 KM • 15+ TEMPLES</span>
            </div>
           
            <div class="hero-icon">🚗</div>
           
            <h1>Divine Karnataka Road Trip</h1>
           
            <p class="hero-subtitle">Pune → Sacred South → Coastal Temples → Mountains → Back Home</p>
           
            <div class="hero-stats">
                <div class="stat-item">
                    <div class="stat-number">7</div>
                    <div class="stat-label">Days</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">1890</div>
                    <div class="stat-label">Kilometers</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">15+</div>
                    <div class="stat-label">Temples</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">6</div>
                    <div class="stat-label">Cities</div>
                </div>
                <div class="stat-item">
                    <div class="stat-number">∞</div>
                    <div class="stat-label">Memories</div>
                </div>
            </div>

            <div class="route-preview">
                <div class="route-stop">🏠 Pune</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🛕 Mangeshi</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🌊 Gokarna</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🗿 Murdeshwar</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🙏 Sringeri</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🌲 Madikeri</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">☕ Chikmagalur</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🏛️ Hampi</div>
                <span class="route-arrow">→</span>
                <div class="route-stop">🏠 Pune</div>
            </div>

            <div class="scroll-indicator">
                <span class="scroll-text">Scroll to Explore</span>
                <div class="scroll-mouse"></div>
            </div>
        </section>

        <!-- DAY 1 -->
        <section class="day-section reveal" id="day1">
            <div class="section-header">
                <div class="section-emoji">🌅</div>
                <h2 class="section-title">Day 1: The Journey Begins</h2>
                <p class="section-subtitle">Pune → Mangeshi Temple, Ponda, Goa</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>01</span>
                    </div>
                    <div class="day-info">
                        <h3>Pune → Mangeshi Temple</h3>
                        <p>Through the majestic Western Ghats to sacred Goa</p>
                    </div>
                    <span class="day-tag tag-temple">🛕 Temple Day</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Distance</div>
                        <div class="info-value">~430 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⏱️</div>
                        <div class="info-label">Drive Time</div>
                        <div class="info-value">8-9 hours</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🌅</div>
                        <div class="info-label">Departure</div>
                        <div class="info-value">5:00 AM</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏁</div>
                        <div class="info-label">Arrival</div>
                        <div class="info-value">4:00 PM</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🛏️</div>
                        <div class="info-label">Night Stay</div>
                        <div class="info-value">Ponda, Goa</div>
                    </div>
                </div>

                <div class="route-box">
                    <h4>🗺️ Today's Route</h4>
                    <div class="route-path">
                        <span>Pune</span>
                        <span class="arrow">→</span>
                        <span>Satara (Breakfast)</span>
                        <span class="arrow">→</span>
                        <span>Kolhapur (Mahalaxmi)</span>
                        <span class="arrow">→</span>
                        <span>Belgaum</span>
                        <span class="arrow">→</span>
                        <span>Anmod Ghat</span>
                        <span class="arrow">→</span>
                        <span>Ponda/Mangeshi</span>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 5:00 AM</div>
                        <div class="timeline-content">
                            <h4>🏠 Departure from Pune</h4>
                            <p>Start early to beat the traffic. Pack snacks, water, and your excitement!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🍳 6:45 AM</div>
                        <div class="timeline-content">
                            <h4>STOP 1: Satara - Breakfast</h4>
                            <p>115 km from Pune | 45 mins break | Try: Misal Pav, Poha at Aaswad Hotel</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🛕 9:30 AM</div>
                        <div class="timeline-content">
                            <h4>STOP 2: Kolhapur Mahalaxmi Temple</h4>
                            <p>One of the Shakti Peethas | 1.5 hrs darshan | Crowd: 🟢 Low in morning</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">☕ 12:45 PM</div>
                        <div class="timeline-content">
                            <h4>STOP 3: Belgaum - Quick Tea</h4>
                            <p>100 km from Kolhapur | 15 mins break | Stretch your legs</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🌲 1:00 PM</div>
                        <div class="timeline-content">
                            <h4>Anmod Ghat - Scenic Drive</h4>
                            <p>Beautiful 95 km ghat road through Western Ghats | 2.5-3 hours | Stop for photos!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏁 4:00 PM</div>
                        <div class="timeline-content">
                            <h4>Arrival at Mangeshi Temple Area</h4>
                            <p>Check-in to hotel, freshen up, and prepare for evening darshan</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🪔 7:00 PM</div>
                        <div class="timeline-content">
                            <h4>⭐ Evening Aarti at Mangeshi Temple</h4>
                            <p>Experience the divine 7-storey Deepstambha lighting! The most magical moment.</p>
                        </div>
                    </div>
                </div>

                <div class="temples-grid">
                    <div class="temple-card">
                        <h4>🛕 Shri Manguesh Temple</h4>
                        <div class="deity">Lord Manguesh (Shiva) | Priol, Ponda</div>
                        <p>Most important Hindu temple in Goa with unique Goan-Portuguese architecture.</p>
                        <div class="temple-features">
                            <span class="temple-feature">7-Storey Deepstambha</span>
                            <span class="temple-feature">Evening Aarti 7PM</span>
                            <span class="temple-feature">Nandi Mandapa</span>
                        </div>
                    </div>
                    <div class="temple-card">
                        <h4>🛕 Shanta Durga Temple</h4>
                        <div class="deity">Goddess Durga | 4 km from Mangeshi</div>
                        <p>Beautiful white temple with pagoda-style architecture. The mediator between Shiva & Vishnu.</p>
                        <div class="temple-features">
                            <span class="temple-feature">White Architecture</span>
                            <span class="temple-feature">Pagoda Style</span>
                            <span class="temple-feature">30-45 mins</span>
                        </div>
                    </div>
                </div>

                <div class="hotels-grid">
                    <div class="hotel-card recommended">
                        <h4>🏨 Goa Woodlands Hotel</h4>
                        <div class="hotel-detail"><span>📍</span> 4 km from temple</div>
                        <div class="hotel-detail"><span>📞</span> 0832-2312151</div>
                        <div class="hotel-detail"><span>✨</span> Clean, good reviews, parking</div>
                        <div class="hotel-price">₹3,000 - ₹5,000</div>
                    </div>
                    <div class="hotel-card">
                        <h4>🏨 Parashuram Deluxe</h4>
                        <div class="hotel-detail"><span>📍</span> 3 km from temple</div>
                        <div class="hotel-detail"><span>📞</span> 0832-2316006</div>
                        <div class="hotel-detail"><span>🥗</span> Pure veg food available</div>
                        <div class="hotel-price">₹2,500 - ₹4,000</div>
                    </div>
                </div>

                <div class="food-grid">
                    <div class="food-item">
                        <div class="food-emoji">🥘</div>
                        <h5>Goan Veg Thali</h5>
                        <p>Rice, curry, sol kadi, pickle</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🥛</div>
                        <h5>Sol Kadi</h5>
                        <p>Kokum-coconut drink</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🥞</div>
                        <h5>Alle Belle</h5>
                        <p>Sweet coconut pancake</p>
                    </div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>🌊</span>
                <span>🐬</span>
                <span>⛵</span>
            </div>
        </div>

        <!-- DAY 2 -->
        <section class="day-section reveal" id="day2">
            <div class="section-header">
                <div class="section-emoji">🌊</div>
                <h2 class="section-title">Day 2: Coastal Temples</h2>
                <p class="section-subtitle">Ponda → Gokarna → Murdeshwar → Sringeri</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>02</span>
                    </div>
                    <div class="day-info">
                        <h3>The Coastal Temple Trail</h3>
                        <p>Experience majestic temples by the Arabian Sea</p>
                    </div>
                    <span class="day-tag tag-coastal">🌊 Coastal Day</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Distance</div>
                        <div class="info-value">~380 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⏱️</div>
                        <div class="info-label">Drive Time</div>
                        <div class="info-value">8-9 hours</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🛕</div>
                        <div class="info-label">Temples</div>
                        <div class="info-value">3 Major</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏁</div>
                        <div class="info-label">Night Stay</div>
                        <div class="info-value">Sringeri</div>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 5:30 AM</div>
                        <div class="timeline-content">
                            <h4>Early Departure from Ponda</h4>
                            <p>Optional: Morning aarti at Mangeshi before leaving</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🛕 8:30 AM</div>
                        <div class="timeline-content">
                            <h4>Gokarna Mahabaleshwar Temple</h4>
                            <p>Mukti Kshetra with the sacred Atmalinga | Dip in Koti Tirtha first | 1 hour darshan</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🗿 11:30 AM</div>
                        <div class="timeline-content">
                            <h4>Murdeshwar Temple</h4>
                            <p>123 ft Shiva statue | 237 ft Gopura | Take the lift for sea views! | 2 hours</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🙏 3:30 PM</div>
                        <div class="timeline-content">
                            <h4>Kollur Mookambika Temple</h4>
                            <p>Shakti Peetha | FREE Anna Daana available | 1.5 hours darshan</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏁 6:30 PM</div>
                        <div class="timeline-content">
                            <h4>Arrival at Sringeri</h4>
                            <p>Check-in and rest at this spiritual headquarters of Shankaracharya</p>
                        </div>
                    </div>
                </div>

                <div class="highlights-box">
                    <h4>📸 Must-Capture Moments</h4>
                    <ul class="highlights-list">
                        <li>Sunrise view at Gokarna Beach</li>
                        <li>Giant Shiva statue against Arabian Sea</li>
                        <li>Gopura lift ride at Murdeshwar</li>
                        <li>Dolphins if you're lucky near the coast!</li>
                    </ul>
                </div>

                <div class="photo-spots">
                    <div class="photo-spot">📸 123ft Shiva Statue</div>
                    <div class="photo-spot">📸 Beach Sunrise</div>
                    <div class="photo-spot">📸 Gopura Top View</div>
                    <div class="photo-spot">📸 Temple Tank</div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>⛰️</span>
                <span>🌲</span>
                <span>🦋</span>
            </div>
        </div>

        <!-- DAY 3 -->
        <section class="day-section reveal" id="day3">
            <div class="section-header">
                <div class="section-emoji">🏔️</div>
                <h2 class="section-title">Day 3: Mountain Temples</h2>
                <p class="section-subtitle">Sringeri → Horanadu → Kalasa → Madikeri</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>03</span>
                    </div>
                    <div class="day-info">
                        <h3>Into the Western Ghats</h3>
                        <p>Sacred temples amidst misty mountains</p>
                    </div>
                    <span class="day-tag tag-mountain">⛰️ Mountain Day</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Distance</div>
                        <div class="info-value">~180 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⏱️</div>
                        <div class="info-label">Drive Time</div>
                        <div class="info-value">5-6 hours</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🌲</div>
                        <div class="info-label">Terrain</div>
                        <div class="info-value">Ghat Roads</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏁</div>
                        <div class="info-label">Night Stay</div>
                        <div class="info-value">Madikeri</div>
                    </div>
                </div>

                <div class="temples-grid">
                    <div class="temple-card">
                        <h4>🛕 Sringeri Sharada Peetham</h4>
                        <div class="deity">Goddess Sharada | Adi Shankaracharya's seat</div>
                        <p>One of the four cardinal mathas. Vidyashankara Temple with unique architecture.</p>
                        <div class="temple-features">
                            <span class="temple-feature">12 Zodiac Pillars</span>
                            <span class="temple-feature">Tunga River</span>
                            <span class="temple-feature">Early Morning Best</span>
                        </div>
                    </div>
                    <div class="temple-card">
                        <h4>🛕 Horanadu  Annapoorneshwari Temple</h4>
                        <div class="deity">Goddess Annapoorneshwari | "No one leaves hungry"</div>
                        <p>Famous for FREE meals to all devotees 24/7. A divine experience of feeding thousands daily.</p>
                        <div class="temple-features">
                            <span class="temple-feature">Free Prasadam 24/7</span>
                            <span class="temple-feature">Mountain Setting</span>
                            <span class="temple-feature">1.5 hrs visit</span>
                        </div>
                    </div>
                    <div class="temple-card">
                        <h4>🛕 Kalasa Kalaseshwara Temple</h4>
                        <div class="deity">Lord Shiva | Bhadra River banks</div>
                        <p>Ancient temple in a serene mountain town. Perfect stop between Horanadu and Madikeri.</p>
                        <div class="temple-features">
                            <span class="temple-feature">River Bathing</span>
                            <span class="temple-feature">Peaceful Atmosphere</span>
                            <span class="temple-feature">45 mins visit</span>
                        </div>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 6:00 AM</div>
                        <div class="timeline-content">
                            <h4>Sringeri Sharada Temple Morning Darshan</h4>
                            <p>Early morning puja at the sacred matha | Walk along Tunga River | Feed the fish!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🛕 9:30 AM</div>
                        <div class="timeline-content">
                            <h4>Horanadu Annapoorneshwari Temple</h4>
                            <p>65 km scenic drive through forests | Don't miss the FREE prasadam lunch here!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏔️ 1:00 PM</div>
                        <div class="timeline-content">
                            <h4>Kalasa Temple Visit</h4>
                            <p>20 km from Horanadu | Quick darshan | Beautiful mountain backdrop</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🌲 3:00 PM</div>
                        <div class="timeline-content">
                            <h4>Drive to Madikeri through Charmadi Ghat</h4>
                            <p>One of the most scenic drives! 60+ hairpin bends | Stop at viewpoints</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏁 6:00 PM</div>
                        <div class="timeline-content">
                            <h4>Arrival at Madikeri (Coorg)</h4>
                            <p>Scotland of India! Check into a coffee estate homestay for the best experience.</p>
                        </div>
                    </div>
                </div>

                <div class="highlights-box">
                    <h4>🌿 Mountain Driving Tips</h4>
                    <ul class="highlights-list">
                        <li>Carry motion sickness medicine for ghat roads</li>
                        <li>Keep headlights on even during daytime</li>
                        <li>Honk at blind curves - safety first!</li>
                        <li>Fill fuel tank before entering ghat sections</li>
                        <li>Expect mobile network issues in some areas</li>
                    </ul>
                </div>

                <div class="hotels-grid">
                    <div class="hotel-card recommended">
                        <h4>🏡 Coorg Wilderness Resort</h4>
                        <div class="hotel-detail"><span>📍</span> 10 km from Madikeri town</div>
                        <div class="hotel-detail"><span>📞</span> 08272-265600</div>
                        <div class="hotel-detail"><span>☕</span> Coffee plantation setting</div>
                        <div class="hotel-price">₹5,000 - ₹8,000</div>
                    </div>
                    <div class="hotel-card">
                        <h4>🏨 Hotel Coorg International</h4>
                        <div class="hotel-detail"><span>📍</span> Madikeri town center</div>
                        <div class="hotel-detail"><span>📞</span> 08272-228071</div>
                        <div class="hotel-detail"><span>🍽️</span> Good restaurant, parking</div>
                        <div class="hotel-price">₹3,500 - ₹5,500</div>
                    </div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>☕</span>
                <span>🌿</span>
                <span>🦜</span>
            </div>
        </div>

        <!-- DAY 4 -->
        <section class="day-section reveal" id="day4">
            <div class="section-header">
                <div class="section-emoji">☕</div>
                <h2 class="section-title">Day 4: Coffee & Nature</h2>
                <p class="section-subtitle">Madikeri → Abbey Falls → Raja's Seat → Chikmagalur</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>04</span>
                    </div>
                    <div class="day-info">
                        <h3>Exploring Coffee Country</h3>
                        <p>Waterfalls, viewpoints & coffee plantations</p>
                    </div>
                    <span class="day-tag tag-mountain">🌲 Nature Day</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Distance</div>
                        <div class="info-value">~160 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⏱️</div>
                        <div class="info-label">Drive Time</div>
                        <div class="info-value">4-5 hours</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🌊</div>
                        <div class="info-label">Attractions</div>
                        <div class="info-value">5 Spots</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏁</div>
                        <div class="info-label">Night Stay</div>
                        <div class="info-value">Chikmagalur</div>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 6:00 AM</div>
                        <div class="timeline-content">
                            <h4>🌅 Sunrise at Raja's Seat</h4>
                            <p>The king's favorite spot! Breathtaking valley views with mist rolling over mountains.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">☕ 8:00 AM</div>
                        <div class="timeline-content">
                            <h4>Breakfast at the homestay</h4>
                            <p>Enjoy authentic Coorgi breakfast - Kadambuttu, Pandi curry (veg options available), filter coffee!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">💧 9:30 AM</div>
                        <div class="timeline-content">
                            <h4>Abbey Falls</h4>
                            <p>8 km from Madikeri | Beautiful waterfall surrounded by coffee plantations | 1 hour visit</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏰 11:00 AM</div>
                        <div class="timeline-content">
                            <h4>Madikeri Fort & Raja's Tomb</h4>
                            <p>Historical fort with elephant gates | Museum inside | 1 hour exploration</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🛕 12:30 PM</div>
                        <div class="timeline-content">
                            <h4>Omkareshwara Temple</h4>
                            <p>Unique blend of Gothic and Islamic architecture | Central tank with fish | 30 mins</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🚗 2:00 PM</div>
                        <div class="timeline-content">
                            <h4>Drive to Chikmagalur</h4>
                            <p>160 km scenic drive through coffee estates | Stop for lunch en route at Hassan</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏁 6:30 PM</div>
                        <div class="timeline-content">
                            <h4>Arrival at Chikmagalur</h4>
                            <p>Birthplace of coffee in India! Check into plantation stay for an aromatic experience.</p>
                        </div>
                    </div>
                </div>

                <div class="food-grid">
                    <div class="food-item">
                        <div class="food-emoji">☕</div>
                        <h5>Filter Coffee</h5>
                        <p>Fresh roasted, local beans</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🍚</div>
                        <h5>Kadambuttu</h5>
                        <p>Coorgi rice dumplings</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🍛</div>
                        <h5>Akki Roti</h5>
                        <p>Rice flatbread with chutney</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🍯</div>
                        <h5>Coorg Honey</h5>
                        <p>Buy to take home!</p>
                    </div>
                </div>

                <div class="photo-spots">
                    <div class="photo-spot">📸 Raja's Seat Sunrise</div>
                    <div class="photo-spot">📸 Abbey Falls</div>
                    <div class="photo-spot">📸 Coffee Plantations</div>
                    <div class="photo-spot">📸 Misty Mountains</div>
                    <div class="photo-spot">📸 Fort Gates</div>
                </div>

                <div class="hotels-grid">
                    <div class="hotel-card recommended">
                        <h4>🏡 Serai Chikmagalur</h4>
                        <div class="hotel-detail"><span>📍</span> Coffee estate, 12 km from town</div>
                        <div class="hotel-detail"><span>📞</span> 08262-220500</div>
                        <div class="hotel-detail"><span>✨</span> Luxury plantation experience</div>
                        <div class="hotel-price">₹8,000 - ₹15,000</div>
                    </div>
                    <div class="hotel-card">
                        <h4>🏨 Hotel Mayura Coffee Land</h4>
                        <div class="hotel-detail"><span>📍</span> Town center, KSTDC property</div>
                        <div class="hotel-detail"><span>📞</span> 08262-234800</div>
                        <div class="hotel-detail"><span>🌿</span> Budget friendly, good location</div>
                        <div class="hotel-price">₹2,500 - ₹4,000</div>
                    </div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>🛕</span>
                <span>🌄</span>
                <span>⭐</span>
            </div>
        </div>

        <!-- DAY 5 -->
        <section class="day-section reveal" id="day5">
            <div class="section-header">
                <div class="section-emoji">⛰️</div>
                <h2 class="section-title">Day 5: Hills & Heritage</h2>
                <p class="section-subtitle">Chikmagalur → Mullayanagiri → Bhadra → Hampi</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>05</span>
                    </div>
                    <div class="day-info">
                        <h3>From Peaks to Ruins</h3>
                        <p>Karnataka's highest peak to UNESCO heritage site</p>
                    </div>
                    <span class="day-tag tag-heritage">🏛️ Heritage Day</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Distance</div>
                        <div class="info-value">~340 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⏱️</div>
                        <div class="info-label">Drive Time</div>
                        <div class="info-value">6-7 hours</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⛰️</div>
                        <div class="info-label">Peak Height</div>
                        <div class="info-value">1,930m</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏛️</div>
                        <div class="info-label">UNESCO Site</div>
                        <div class="info-value">Hampi</div>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 5:00 AM</div>
                        <div class="timeline-content">
                            <h4>⛰️ Mullayanagiri Peak Trek</h4>
                            <p>Karnataka's highest peak! 22 km from Chikmagalur | 1.5 km easy trek to summit | Sunrise views are magical!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">☕ 8:30 AM</div>
                        <div class="timeline-content">
                            <h4>Breakfast at Plantation Café</h4>
                            <p>Hot coffee with misty mountain views | Try the local breakfast specials</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🦌 10:00 AM</div>
                        <div class="timeline-content">
                            <h4>Bhadra Wildlife Sanctuary (Optional)</h4>
                            <p>Quick stop at the sanctuary gate | If time permits, short nature walk | Spot deer, elephants!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🚗 11:30 AM</div>
                        <div class="timeline-content">
                            <h4>Long Drive to Hampi</h4>
                            <p>280 km journey through Karnataka's heartland | Lunch stop at Davangere - try the famous Benne Dosa!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🌅 5:30 PM</div>
                        <div class="timeline-content">
                            <h4>Arrival at Hampi</h4>
                            <p>Check-in near Virupaksha Temple | Evening stroll in the bazaar ruins</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🗿 6:30 PM</div>
                        <div class="timeline-content">
                            <h4>Sunset at Hemakuta Hill</h4>
                            <p>Most spectacular sunset spot in Hampi! Panoramic views of Virupaksha Temple & boulder landscape.</p>
                        </div>
                    </div>
                </div>

                <div class="highlights-box">
                    <h4>🏛️ About Hampi</h4>
                    <ul class="highlights-list">
                        <li>UNESCO World Heritage Site since 1986</li>
                        <li>Capital of the mighty Vijayanagara Empire (1336-1646 AD)</li>
                        <li>Spread across 26 sq km with 500+ monuments</li>
                        <li>One of the world's largest open-air museums</li>
                        <li>Best explored over 2 days minimum</li>
                    </ul>
                </div>

                <div class="hotels-grid">
                    <div class="hotel-card recommended">
                        <h4>🏨 Evolve Back Hampi</h4>
                        <div class="hotel-detail"><span>📍</span> Kamalapur, 3 km from ruins</div>
                        <div class="hotel-detail"><span>📞</span> 08394-241010</div>
                        <div class="hotel-detail"><span>✨</span> Luxury heritage resort</div>
                        <div class="hotel-price">₹12,000 - ₹25,000</div>
                    </div>
                    <div class="hotel-card">
                        <h4>🏨 Clarks Inn Hampi</h4>
                        <div class="hotel-detail"><span>📍</span> Near Virupaksha Temple</div>
                        <div class="hotel-detail"><span>📞</span> 08394-241200</div>
                        <div class="hotel-detail"><span>🛕</span> Walking distance to temples</div>
                        <div class="hotel-price">₹3,500 - ₹6,000</div>
                    </div>
                    <div class="hotel-card">
                        <h4>🏡 Hampi Guesthouse</h4>
                        <div class="hotel-detail"><span>📍</span> Hampi Bazaar</div>
                        <div class="hotel-detail"><span>📞</span> 08394-241695</div>
                        <div class="hotel-detail"><span>🎒</span> Budget, great location</div>
                        <div class="hotel-price">₹1,500 - ₹3,000</div>
                    </div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>🏛️</span>
                <span>🗿</span>
                <span>👑</span>
            </div>
        </div>

        <!-- DAY 6 -->
        <section class="day-section reveal" id="day6">
            <div class="section-header">
                <div class="section-emoji">🏛️</div>
                <h2 class="section-title">Day 6: Hampi Exploration</h2>
                <p class="section-subtitle">Full Day at the Vijayanagara Empire Ruins</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>06</span>
                    </div>
                    <div class="day-info">
                        <h3>Walking Through History</h3>
                        <p>Explore the magnificent ruins of a forgotten empire</p>
                    </div>
                    <span class="day-tag tag-heritage">🏛️ Full Exploration</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">🏛️</div>
                        <div class="info-label">Monuments</div>
                        <div class="info-value">15+ Sites</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🚶</div>
                        <div class="info-label">Walking</div>
                        <div class="info-value">8-10 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🚗</div>
                        <div class="info-label">Method</div>
                        <div class="info-value">Car + Walk</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏁</div>
                        <div class="info-label">Night Stay</div>
                        <div class="info-value">Hampi</div>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 6:00 AM</div>
                        <div class="timeline-content">
                            <h4>🌅 Sunrise at Virupaksha Temple</h4>
                            <p>Witness the sun rays falling on the temple gopura. Feed the temple elephant Lakshmi!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🍳 7:30 AM</div>
                        <div class="timeline-content">
                            <h4>Breakfast at Mango Tree Restaurant</h4>
                            <p>Iconic riverside café with boulder views | Try the banana pancakes!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🗿 9:00 AM</div>
                        <div class="timeline-content">
                            <h4>Vittala Temple Complex</h4>
                            <p>The famous Stone Chariot & Musical Pillars! Most photographed monument. 2 hours minimum.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏛️ 11:30 AM</div>
                        <div class="timeline-content">
                            <h4>King's Balance & Achyutaraya Temple</h4>
                            <p>Where kings were weighed against gold! Quieter temple with amazing architecture.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🍽️ 1:00 PM</div>
                        <div class="timeline-content">
                            <h4>Lunch Break</h4>
                            <p>Return to hotel or eat at a local restaurant. Rest during peak afternoon heat!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏰 3:30 PM</div>
                        <div class="timeline-content">
                            <h4>Royal Enclosure Area</h4>
                            <p>Lotus Mahal, Elephant Stables, Underground Temple, Queen's Bath - must see!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🗿 5:00 PM</div>
                        <div class="timeline-content">
                            <h4>Ugra Narasimha & Badavilinga</h4>
                            <p>Massive 6.7m Narasimha statue carved from single boulder. Incredible craftsmanship!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🌅 6:30 PM</div>
                        <div class="timeline-content">
                            <h4>Sunset at Matanga Hill</h4>
                            <p>Climb 573 steps for the BEST view of Hampi! 360° panorama of the entire site.</p>
                        </div>
                    </div>
                </div>

                <div class="temples-grid">
                    <div class="temple-card">
                        <h4>🛕 Virupaksha Temple</h4>
                        <div class="deity">Lord Shiva (Virupaksha)</div>
                        <p>Still an active temple! 160 ft gopuram, beautiful mantapas, sacred tank.</p>
                        <div class="temple-features">
                            <span class="temple-feature">7th Century</span>
                            <span class="temple-feature">Active Worship</span>
                            <span class="temple-feature">Temple Elephant</span>
                        </div>
                    </div>
                    <div class="temple-card">
                        <h4>🗿 Vittala Temple</h4>
                        <div class="deity">Lord Vittala (Vishnu)</div>
                        <p>Home to the iconic Stone Chariot and Musical Pillars that produce musical notes!</p>
                        <div class="temple-features">
                            <span class="temple-feature">Stone Chariot</span>
                            <span class="temple-feature">Musical Pillars</span>
                            <span class="temple-feature">UNESCO Highlight</span>
                        </div>
                    </div>
                    <div class="temple-card">
                        <h4>🏰 Royal Enclosure</h4>
                        <div class="deity">Administrative Complex</div>
                        <p>Lotus Mahal, Elephant Stables, Underground Temple - witness the grandeur of royalty!</p>
                        <div class="temple-features">
                            <span class="temple-feature">Lotus Mahal</span>
                            <span class="temple-feature">11 Elephant Stables</span>
                            <span class="temple-feature">Queen's Bath</span>
                        </div>
                    </div>
                </div>

                <div class="tips-grid">
                    <div class="tip-card">
                        <div class="tip-number">1</div>
                        <div class="tip-content">
                            <h5>Start Early</h5>
                            <p>Hampi gets very hot! Best explored before 11 AM and after 4 PM.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">2</div>
                        <div class="tip-content">
                            <h5>Hire a Guide</h5>
                            <p>₹800-1500 for full day. They bring the ruins to life with stories!</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">3</div>
                        <div class="tip-content">
                            <h5>Wear Comfortable Shoes</h5>
                            <p>Lots of walking on uneven terrain. Carry water & sunscreen.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">4</div>
                        <div class="tip-content">
                            <h5>Respect the Site</h5>
                            <p>Don't climb on ruins or remove stones. It's a protected heritage.</p>
                        </div>
                    </div>
                </div>

                <div class="photo-spots">
                    <div class="photo-spot">📸 Stone Chariot</div>
                    <div class="photo-spot">📸 Lotus Mahal</div>
                    <div class="photo-spot">📸 Matanga Hill View</div>
                    <div class="photo-spot">📸 Virupaksha Gopura</div>
                    <div class="photo-spot">📸 Boulder Landscape</div>
                    <div class="photo-spot">📸 Coracle Ride</div>
                </div>

                <div class="food-grid">
                    <div class="food-item">
                        <div class="food-emoji">🍌</div>
                        <h5>Banana Pancakes</h5>
                        <p>Mango Tree specialty</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🥘</div>
                        <h5>North Karnataka Thali</h5>
                        <p>Jowar roti, brinjal curry</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🥤</div>
                        <h5>Fresh Coconut Water</h5>
                        <p>Beat the heat!</p>
                    </div>
                    <div class="food-item">
                        <div class="food-emoji">🍦</div>
                        <h5>Mango Lassi</h5>
                        <p>Refreshing treat</p>
                    </div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>🏠</span>
                <span>🚗</span>
                <span>💫</span>
            </div>
        </div>

        <!-- DAY 7 -->
        <section class="day-section reveal" id="day7">
            <div class="section-header">
                <div class="section-emoji">🏠</div>
                <h2 class="section-title">Day 7: Homeward Bound</h2>
                <p class="section-subtitle">Hampi → Pune | The Journey Home</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="day-header">
                    <div class="day-badge">
                        <span>Day</span>
                        <span>07</span>
                    </div>
                    <div class="day-info">
                        <h3>Return with Beautiful Memories</h3>
                        <p>Final leg of the divine Karnataka journey</p>
                    </div>
                    <span class="day-tag tag-return">🏠 Return Journey</span>
                </div>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Distance</div>
                        <div class="info-value">~400 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⏱️</div>
                        <div class="info-label">Drive Time</div>
                        <div class="info-value">7-8 hours</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🛣️</div>
                        <div class="info-label">Route</div>
                        <div class="info-value">NH48</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🎯</div>
                        <div class="info-label">ETA Home</div>
                        <div class="info-value">~6:00 PM</div>
                    </div>
                </div>

                <div class="route-box">
                    <h4>🗺️ Return Route</h4>
                    <div class="route-path">
                        <span>Hampi</span>
                        <span class="arrow">→</span>
                        <span>Hospet (15 km)</span>
                        <span class="arrow">→</span>
                        <span>Hubli (130 km)</span>
                        <span class="arrow">→</span>
                        <span>Belgaum (90 km)</span>
                        <span class="arrow">→</span>
                        <span>Kolhapur (100 km)</span>
                        <span class="arrow">→</span>
                        <span>Pune (230 km)</span>
                    </div>
                </div>

                <div class="timeline">
                    <div class="timeline-item">
                        <div class="timeline-time">⏰ 6:30 AM</div>
                        <div class="timeline-content">
                            <h4>Early Morning Darshan (Optional)</h4>
                            <p>Final visit to Virupaksha Temple. Seek blessings for a safe journey home.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🍳 7:30 AM</div>
                        <div class="timeline-content">
                            <h4>Breakfast & Check-out</h4>
                            <p>Pack your bags, settle bills, and prepare for the drive home.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🚗 8:30 AM</div>
                        <div class="timeline-content">
                            <h4>Depart from Hampi</h4>
                            <p>Drive to Hospet (15 km) and join NH48 towards Pune.</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">☕ 11:00 AM</div>
                        <div class="timeline-content">
                            <h4>Tea Break at Hubli</h4>
                            <p>130 km from Hampi | 20 mins break | Clean restrooms at Café Coffee Day</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🍽️ 1:30 PM</div>
                        <div class="timeline-content">
                            <h4>Lunch at Belgaum</h4>
                            <p>90 km from Hubli | Try the famous Belgaum Kunda (sweet) as a takeaway!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🛕 3:30 PM</div>
                        <div class="timeline-content">
                            <h4>Quick Stop at Kolhapur (Optional)</h4>
                            <p>If time permits, quick darshan at Mahalaxmi Temple again for full circle!</p>
                        </div>
                    </div>
                    <div class="timeline-item">
                        <div class="timeline-time">🏠 6:00 PM</div>
                        <div class="timeline-content">
                            <h4>Arrival at Pune! 🎉</h4>
                            <p>Home sweet home! Unpack, rest, and relive the beautiful memories.</p>
                        </div>
                    </div>
                </div>

                <div class="highlights-box">
                    <h4>🛍️ Things to Buy & Take Home</h4>
                    <ul class="highlights-list">
                        <li>🍯 Coorg Honey & Coffee from Madikeri/Chikmagalur</li>
                        <li>🌶️ Goan Spices & Bebinca from Goa</li>
                        <li>🍬 Belgaum Kunda (famous milk sweet)</li>
                        <li>🎨 Hampi Stone Carvings (miniatures from local shops)</li>
                        <li>🪔 Temple Prasad from all visited temples</li>
                        <li>🧵 Kasuti Embroidery (North Karnataka specialty)</li>
                    </ul>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>📊</span>
                <span>📋</span>
                <span>✅</span>
            </div>
        </div>

        <!-- TRIP SUMMARY -->
        <section class="day-section reveal" id="summary">
            <div class="section-header">
                <div class="section-emoji">📊</div>
                <h2 class="section-title">Trip Summary</h2>
                <p class="section-subtitle">Complete Overview of Your Divine Journey</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <table class="summary-table">
                    <thead>
                        <tr>
                            <th>Day</th>
                            <th>Route</th>
                            <th>Distance</th>
                            <th>Highlights</th>
                            <th>Stay</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td><strong>Day 1</strong></td>
                            <td>Pune → Mangeshi, Goa</td>
                            <td>430 km</td>
                            <td>Kolhapur Mahalaxmi, Mangeshi Temple</td>
                            <td>Ponda</td>
                        </tr>
                        <tr>
                            <td><strong>Day 2</strong></td>
                            <td>Goa → Gokarna → Sringeri</td>
                            <td>380 km</td>
                            <td>Gokarna, Murdeshwar, Mookambika</td>
                            <td>Sringeri</td>
                        </tr>
                        <tr>
                            <td><strong>Day 3</strong></td>
                            <td>Sringeri → Horanadu → Madikeri</td>
                            <td>180 km</td>
                            <td>Sharada Peetham, Annapoorneshwari</td>
                            <td>Madikeri</td>
                        </tr>
                        <tr>
                            <td><strong>Day 4</strong></td>
                            <td>Madikeri → Chikmagalur</td>
                            <td>160 km</td>
                            <td>Abbey Falls, Raja's Seat, Coffee Estates</td>
                            <td>Chikmagalur</td>
                        </tr>
                        <tr>
                            <td><strong>Day 5</strong></td>
                            <td>Chikmagalur → Hampi</td>
                            <td>340 km</td>
                            <td>Mullayanagiri Peak, Bhadra Wildlife</td>
                            <td>Hampi</td>
                        </tr>
                        <tr>
                            <td><strong>Day 6</strong></td>
                            <td>Hampi Exploration</td>
                            <td>~20 km</td>
                            <td>Vittala, Royal Enclosure, Matanga Hill</td>
                            <td>Hampi</td>
                        </tr>
                        <tr>
                            <td><strong>Day 7</strong></td>
                            <td>Hampi → Pune</td>
                            <td>400 km</td>
                            <td>Scenic drive through Karnataka</td>
                            <td>Home!</td>
                        </tr>
                    </tbody>
                </table>

                <div class="info-grid">
                    <div class="info-item">
                        <div class="info-icon">📏</div>
                        <div class="info-label">Total Distance</div>
                        <div class="info-value">~1,890 km</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">⛽</div>
                        <div class="info-label">Est. Fuel Cost</div>
                        <div class="info-value">₹12,000-15,000</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🏨</div>
                        <div class="info-label">Est. Stay Cost</div>
                        <div class="info-value">₹20,000-35,000</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">🍽️</div>
                        <div class="info-label">Est. Food Cost</div>
                        <div class="info-value">₹8,000-12,000</div>
                    </div>
                    <div class="info-item">
                        <div class="info-icon">💰</div>
                        <div class="info-label">Total Budget</div>
                        <div class="info-value">₹45,000-65,000</div>
                    </div>
                </div>
            </div>
        </section>

        <div class="section-divider">
            <div class="divider-icons">
                <span>📝</span>
                <span>✨</span>
                <span>💡</span>
            </div>
        </div>

        <!-- TIPS & ESSENTIALS -->
        <section class="day-section reveal" id="tips">
            <div class="section-header">
                <div class="section-emoji">💡</div>
                <h2 class="section-title">Tips & Essentials</h2>
                <p class="section-subtitle">Everything You Need to Know</p>
                <div class="decorative-line"></div>
            </div>

            <div class="day-card">
                <div class="highlights-box">
                    <h4>🎒 Packing Checklist</h4>
                    <ul class="highlights-list">
                        <li>Comfortable walking shoes (lots of temple visits!)</li>
                        <li>Traditional attire for temples (avoid shorts/sleeveless)</li>
                        <li>Rain jacket/umbrella (Western Ghats can be unpredictable)</li>
                        <li>Sunscreen, sunglasses, cap for Hampi</li>
                        <li>Power bank & car charger for phones</li>
                        <li>Basic medicines & first aid kit</li>
                        <li>Camera/GoPro for memories</li>
                        <li>Cash (many places don't accept cards)</li>
                    </ul>
                </div>

                <div class="tips-grid">
                    <div class="tip-card">
                        <div class="tip-number">⛽</div>
                        <div class="tip-content">
                            <h5>Fuel Tips</h5>
                            <p>Fill tank at Indian Oil/HP stations. Avoid remote petrol pumps. Keep tank above 25%.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">📱</div>
                        <div class="tip-content">
                            <h5>Network Issues</h5>
                            <p>Jio works best in ghats. Download offline maps. Airtel has good coverage overall.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">🚗</div>
                        <div class="tip-content">
                            <h5>Car Preparation</h5>
                            <p>Full service before trip. Check tyres, brakes. Carry spare tyre, jack, basic tools.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">🛕</div>
                        <div class="tip-content">
                            <h5>Temple Etiquette</h5>
                            <p>Remove footwear, maintain silence, dress modestly. Photography rules vary - check first.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">☀️</div>
                        <div class="tip-content">
                            <h5>Best Season</h5>
                            <p>October to March is ideal. Avoid peak summer (April-May) especially for Hampi.</p>
                        </div>
                    </div>
                    <div class="tip-card">
                        <div class="tip-number">💊</div>
                        <div class="tip-content">
                            <h5>Health Tips</h5>
                            <p>Carry motion sickness pills for ghats. Stay hydrated. Avoid street food if sensitive.</p>
                        </div>
                    </div>
                </div>

                <div class="contacts-grid">
                    <div class="contact-card">
                        <div class="contact-icon">🚨</div>
                        <div class="contact-info">
                            <strong>Emergency</strong>
                            <span>112 (All India)</span>
                        </div>
                    </div>
                    <div class="contact-card">
                        <div class="contact-icon">🏥</div>
                        <div class="contact-info">
                            <strong>Ambulance</strong>
                            <span>108</span>
                        </div>
                    </div>
                    <div class="contact-card">
                        <div class="contact-icon">🚔</div>
                        <div class="contact-info">
                            <strong>Police</strong>
                            <span>100</span>
                        </div>
                    </div>
                    <div class="contact-card">
                        <div class="contact-icon">🚗</div>
                        <div class="contact-info">
                            <strong>Road Assistance</strong>
                            <span>1800-180-1111</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- FOOTER -->
        <footer class="footer reveal">
            <div class="footer-emoji">🙏</div>
            <div class="footer-text">शुभ यात्रा! (Shubh Yatra!)</div>
            <div class="footer-subtext">May your journey be blessed with divine experiences and beautiful memories!</div>
            
            <div class="footer-stats">
                <span>🚗 1,890 km of Adventure</span>
                <span>🛕 15+ Sacred Temples</span>
                <span>⛰️ Mountains to Beaches</span>
                <span>☕ Coffee Country</span>
                <span>🏛️ UNESCO Heritage</span>
            </div>

            <div style="margin-top: 40px; padding-top: 30px; border-top: 1px solid rgba(255,215,0,0.2);">
                <p style="color: #666; font-size: 0.85rem;">
                    Made with ❤️ for road trip enthusiasts<br>
                    <span style="font-size: 0.75rem;">Last updated: 2024 | Distances are approximate</span>
                </p>
            </div>
        </footer>
    </div>

    <script>
        // Scroll Reveal Animation
        function revealOnScroll() {
            const reveals = document.querySelectorAll('.reveal');
            
            reveals.forEach(element => {
                const windowHeight = window.innerHeight;
                const elementTop = element.getBoundingClientRect().top;
                const elementVisible = 150;
                
                if (elementTop < windowHeight - elementVisible) {
                    element.classList.add('active');
                }
            });
        }

        window.addEventListener('scroll', revealOnScroll);
        window.addEventListener('load', revealOnScroll);

        // Cursor Trail Effect
        const colors = ['#ff6b35', '#ffd700', '#ff8c00', '#00b4d8', '#90EE90'];
        let colorIndex = 0;

        document.addEventListener('mousemove', (e) => {
            // Throttle the effect
            if (Math.random() > 0.85) {
                const trail = document.createElement('div');
                trail.className = 'cursor-trail';
                trail.style.left = e.clientX - 10 + 'px';
                trail.style.top = e.clientY - 10 + 'px';
                trail.style.background = colors[colorIndex % colors.length];
                document.body.appendChild(trail);
                colorIndex++;
                
                setTimeout(() => {
                    trail.remove();
                }, 1000);
            }
        });

        // Smooth Scroll for Route Stops
        document.querySelectorAll('.route-stop').forEach(stop => {
            stop.addEventListener('click', function() {
                const text = this.textContent.toLowerCase();
                let targetId = '';
                
                if (text.includes('gokarna') || text.includes('murdeshwar')) targetId = 'day2';
                else if (text.includes('sringeri')) targetId = 'day3';
                else if (text.includes('madikeri')) targetId = 'day4';
                else if (text.includes('chikmagalur')) targetId = 'day5';
                else if (text.includes('hampi')) targetId = 'day6';
                else if (text.includes('mangeshi')) targetId = 'day1';
                
                if (targetId) {
                    document.getElementById(targetId)?.scrollIntoView({ behavior: 'smooth' });
                }
            });
        });

        // Parallax Effect for Background Elements
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            
            // Move sun slightly
            const sun = document.querySelector('.sun');
            if (sun) {
                sun.style.transform = `translateY(${scrolled * 0.1}px)`;
            }
            
            // Move clouds at different speeds
            document.querySelectorAll('.cloud').forEach((cloud, i) => {
                cloud.style.transform = `translateX(${scrolled * (0.05 + i * 0.02)}px)`;
            });
        });

        // Add active state to navigation on scroll
        const sections = document.querySelectorAll('.day-section');
        const navDots = [];

        // Create navigation dots
        const navContainer = document.createElement('div');
        navContainer.style.cssText = `
            position: fixed;
            right: 20px;
            top: 50%;
            transform: translateY(-50%);
            z-index: 1000;
            display: flex;
            flex-direction: column;
            gap: 10px;
        `;

        sections.forEach((section, index) => {
            const dot = document.createElement('div');
            dot.style.cssText = `
                width: 12px;
                height: 12px;
                border-radius: 50%;
                background: rgba(255, 215, 0, 0.3);
                border: 2px solid var(--temple-gold);
                cursor: pointer;
                transition: all 0.3s ease;
            `;
            dot.title = `Day ${index + 1}`;
            dot.addEventListener('click', () => {
                section.scrollIntoView({ behavior: 'smooth' });
            });
            navDots.push(dot);
            navContainer.appendChild(dot);
        });

        document.body.appendChild(navContainer);

        // Update active dot on scroll
        window.addEventListener('scroll', () => {
            let current = '';
            
            sections.forEach((section, index) => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                
                if (window.pageYOffset >= sectionTop - 300) {
                    current = index;
                }
            });
            
            navDots.forEach((dot, index) => {
                if (index === current) {
                    dot.style.background = 'var(--temple-gold)';
                    dot.style.transform = 'scale(1.3)';
                } else {
                    dot.style.background = 'rgba(255, 215, 0, 0.3)';
                    dot.style.transform = 'scale(1)';
                }
            });
        });

        // Easter egg: Konami code for confetti
        let konamiCode = [];
        const konamiPattern = [38, 38, 40, 40, 37, 39, 37, 39, 66, 65];
        
        document.addEventListener('keydown', (e) => {
            konamiCode.push(e.keyCode);
            konamiCode = konamiCode.slice(-10);
            
            if (konamiCode.join(',') === konamiPattern.join(',')) {
                celebrateTrip();
            }
        });

        function celebrateTrip() {
            const emojis = ['🎉', '🎊', '✨', '🌟', '🚗', '🛕', '🌴', '⛰️', '🌊', '☕'];
            
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const emoji = document.createElement('div');
                    emoji.textContent = emojis[Math.floor(Math.random() * emojis.length)];
                    emoji.style.cssText = `
                        position: fixed;
                        left: ${Math.random() * 100}vw;
                        top: -50px;
                        font-size: ${20 + Math.random() * 30}px;
                        z-index: 10000;
                        pointer-events: none;
                        animation: confettiFall ${3 + Math.random() * 2}s linear forwards;
                    `;
                    document.body.appendChild(emoji);
                    
                    setTimeout(() => emoji.remove(), 5000);
                }, i * 100);
            }
        }

        // Add confetti animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes confettiFall {
                0% {
                    transform: translateY(0) rotate(0deg);
                    opacity: 1;
                }
                100% {
                    transform: translateY(100vh) rotate(720deg);
                    opacity: 0;
                }
            }
        `;
        document.head.appendChild(style);

        // Console welcome message
        console.log(`
        🚗 Divine Karnataka Road Trip 🛕
        ================================
        Welcome, fellow traveler!
        
        This itinerary covers:
        📍 1,890 km of scenic roads
        🛕 15+ sacred temples
        ⛰️ Mountains, beaches & heritage
        
        Tip: Press ↑↑↓↓←→←→BA for a surprise!
        
        शुभ यात्रा! (Shubh Yatra!)
        `);
    </script>
</body>
</html>
