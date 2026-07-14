<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KARTHIKEYAN S | AI ENGINEER OS v6.0</title>
    <style>
        :root {
            --bg: #0a0a14;
            --surface: #0f172a;
            --neon: #00ff9d;
            --neon2: #00d4ff;
            --deep: #1e1b4b;
            --text: #8892b0;
            --danger: #ff3366;
            --warning: #ffaa00;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: var(--bg);
            color: var(--text);
            font-family: 'Fira Code', 'Courier New', monospace;
            overflow-x: hidden;
            line-height: 1.6;
            cursor: crosshair;
        }

        /* ── SCANLINES ── */
        .scanlines {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0, 255, 157, 0.015) 2px, rgba(0, 255, 157, 0.015) 4px);
            pointer-events: none;
            z-index: 9999;
        }

        /* ── CUSTOM CURSOR TRAIL ── */
        .cursor-trail {
            position: fixed;
            width: 8px;
            height: 8px;
            background: var(--neon);
            border-radius: 50%;
            pointer-events: none;
            z-index: 9998;
            box-shadow: 0 0 20px var(--neon), 0 0 60px var(--neon);
            animation: trailFade 0.8s ease-out forwards;
        }
        @keyframes trailFade {
            to {
                opacity: 0;
                transform: scale(0);
            }
        }

        /* ── BOOT SCREEN ── */
        .boot-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100vh;
            background: var(--bg);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 10000;
            animation: fadeOut 0.6s ease-in-out 3.5s forwards;
        }
        @keyframes fadeOut {
            to {
                opacity: 0;
                visibility: hidden;
            }
        }
        .boot-text {
            color: var(--neon);
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 4px;
            text-shadow: 0 0 30px var(--neon), 0 0 60px var(--neon);
            animation: glitchText 0.3s infinite;
        }
        @keyframes glitchText {
            0%,
            100% {
                transform: translate(0);
            }
            20% {
                transform: translate(-3px, 3px);
                text-shadow: 3px 0 var(--danger), -3px 0 var(--neon2);
            }
            40% {
                transform: translate(3px, -3px);
            }
            60% {
                transform: translate(-3px, -3px);
                text-shadow: -3px 0 var(--danger), 3px 0 var(--neon2);
            }
            80% {
                transform: translate(3px, 3px);
            }
        }
        .boot-sub {
            color: var(--text);
            font-size: 0.85rem;
            margin-top: 12px;
            letter-spacing: 2px;
        }
        .boot-bar {
            width: 300px;
            height: 4px;
            background: rgba(0, 255, 157, 0.15);
            border-radius: 2px;
            margin-top: 25px;
            overflow: hidden;
            position: relative;
        }
        .boot-bar-fill {
            width: 0;
            height: 100%;
            background: linear-gradient(90deg, var(--neon), var(--neon2), var(--neon));
            border-radius: 2px;
            animation: fillBar 2.2s ease-in-out forwards;
            box-shadow: 0 0 20px var(--neon);
        }
        @keyframes fillBar {
            to {
                width: 100%;
            }
        }
        .boot-spinner {
            width: 55px;
            height: 55px;
            border: 2px solid rgba(0, 255, 157, 0.2);
            border-top-color: var(--neon);
            border-right-color: var(--neon2);
            border-radius: 50%;
            margin-top: 30px;
            animation: spin 0.8s linear infinite;
        }
        @keyframes spin {
            to {
                transform: rotate(360deg);
            }
        }
        .boot-welcome {
            color: var(--neon);
            font-size: 0.75rem;
            margin-top: 25px;
            opacity: 0;
            animation: welcomeIn 0.5s ease-out 2.5s forwards;
        }
        @keyframes welcomeIn {
            to {
                opacity: 1;
                letter-spacing: 3px;
            }
        }

        /* ── CONTAINER ── */
        .container {
            max-width: 950px;
            margin: 0 auto;
            padding: 20px;
        }

        /* ── HEADER / HOLOGRAM ── */
        .header {
            text-align: center;
            padding: 50px 20px 30px;
            position: relative;
        }
        .hologram {
            position: relative;
            width: 320px;
            height: 320px;
            margin: 0 auto 20px;
            perspective: 1000px;
        }
        .holo-ring {
            position: absolute;
            top: 50%;
            left: 50%;
            border-radius: 50%;
            border: 2px solid rgba(0, 255, 157, 0.4);
            transform: translate(-50%, -50%);
            animation: ringPulse 3s ease-in-out infinite;
        }
        .holo-ring:nth-child(1) {
            width: 280px;
            height: 280px;
            animation-delay: 0s;
        }
        .holo-ring:nth-child(2) {
            width: 200px;
            height: 200px;
            animation-delay: 0.5s;
            border-color: rgba(0, 212, 255, 0.3);
        }
        .holo-ring:nth-child(3) {
            width: 120px;
            height: 120px;
            animation-delay: 1s;
            border-color: rgba(0, 255, 157, 0.6);
        }
        @keyframes ringPulse {
            0%,
            100% {
                box-shadow: 0 0 15px rgba(0, 255, 157, 0.2);
            }
            50% {
                box-shadow: 0 0 40px rgba(0, 255, 157, 0.5), 0 0 80px rgba(0, 212, 255, 0.3);
            }
        }
        .cube-wrapper {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            transform-style: preserve-3d;
            animation: floatCube 6s ease-in-out infinite;
        }
        @keyframes floatCube {
            0%,
            100% {
                transform: translate(-50%, -50%) rotateX(0deg) rotateY(0deg);
            }
            33% {
                transform: translate(-50%, -55%) rotateX(10deg) rotateY(120deg);
            }
            66% {
                transform: translate(-50%, -45%) rotateX(-10deg) rotateY(240deg);
            }
        }
        .cube {
            width: 140px;
            height: 140px;
            transform-style: preserve-3d;
            animation: rotateCube 25s linear infinite;
        }
        @keyframes rotateCube {
            to {
                transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg);
            }
        }
        .cube-face {
            position: absolute;
            width: 140px;
            height: 140px;
            border: 2px solid var(--neon);
            box-shadow: 0 0 25px rgba(0, 255, 157, 0.3), inset 0 0 25px rgba(0, 255, 157, 0.08);
            background: rgba(0, 255, 157, 0.02);
        }
        .cf {
            transform: translateZ(70px);
        }
        .cb {
            transform: rotateY(180deg) translateZ(70px);
        }
        .cl {
            transform: rotateY(-90deg) translateZ(70px);
        }
        .cr {
            transform: rotateY(90deg) translateZ(70px);
        }
        .ct {
            transform: rotateX(90deg) translateZ(70px);
        }
        .cbo {
            transform: rotateX(-90deg) translateZ(70px);
        }
        .inner-cube {
            position: absolute;
            width: 90px;
            height: 90px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            transform-style: preserve-3d;
        }
        .inner-face {
            position: absolute;
            width: 90px;
            height: 90px;
            border: 1.5px solid rgba(0, 255, 157, 0.5);
            background: rgba(0, 255, 157, 0.03);
        }
        .icf {
            transform: translateZ(45px);
        }
        .icb {
            transform: rotateY(180deg) translateZ(45px);
        }
        .icl {
            transform: rotateY(-90deg) translateZ(45px);
        }
        .icr {
            transform: rotateY(90deg) translateZ(45px);
        }
        .ict {
            transform: rotateX(90deg) translateZ(45px);
        }
        .icbo {
            transform: rotateX(-90deg) translateZ(45px);
        }
        .particles {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
        }
        .particle {
            position: absolute;
            width: 5px;
            height: 5px;
            background: var(--neon);
            border-radius: 50%;
            box-shadow: 0 0 15px var(--neon);
        }
        .p1 {
            top: 10%;
            left: 20%;
            animation: floatP1 5s ease-in-out infinite;
        }
        .p2 {
            top: 70%;
            left: 75%;
            animation: floatP2 4.5s ease-in-out infinite 0.8s;
        }
        .p3 {
            top: 80%;
            left: 15%;
            animation: floatP1 5.5s ease-in-out infinite 1.5s;
        }
        .p4 {
            top: 25%;
            left: 80%;
            animation: floatP2 4s ease-in-out infinite 2s;
        }
        .p5 {
            top: 50%;
            left: 50%;
            animation: floatP1 6s ease-in-out infinite 0.5s;
        }
        .p6 {
            top: 5%;
            left: 60%;
            animation: floatP2 5s ease-in-out infinite 2.5s;
        }
        @keyframes floatP1 {
            0%,
            100% {
                transform: translate(0, 0);
                opacity: 0.3;
            }
            25% {
                transform: translate(15px, -20px);
                opacity: 1;
            }
            50% {
                transform: translate(-8px, -35px);
                opacity: 0.5;
            }
            75% {
                transform: translate(-20px, -10px);
                opacity: 0.8;
            }
        }
        @keyframes floatP2 {
            0%,
            100% {
                transform: translate(0, 0);
                opacity: 0.3;
            }
            25% {
                transform: translate(-12px, -25px);
                opacity: 1;
            }
            50% {
                transform: translate(10px, -15px);
                opacity: 0.6;
            }
            75% {
                transform: translate(18px, 5px);
                opacity: 0.8;
            }
        }
        .title-name {
            font-size: 2.8rem;
            font-weight: bold;
            background: linear-gradient(135deg, var(--neon) 0%, var(--neon2) 30%, var(--neon) 60%, var(--deep) 80%, var(--neon) 100%);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: titleShimmer 4s ease-in-out infinite;
        }
        @keyframes titleShimmer {
            0%,
            100% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
        }
        .subtitle {
            color: var(--neon);
            font-size: 0.9rem;
            opacity: 0.7;
            margin-top: 6px;
            letter-spacing: 2px;
        }
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            justify-content: center;
            margin: 20px 0;
        }
        .badge {
            background: transparent;
            color: var(--neon);
            border: 1.5px solid var(--neon);
            padding: 10px 20px;
            border-radius: 2px;
            font-size: 0.8rem;
            text-decoration: none;
            letter-spacing: 1px;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        .badge::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 157, 0.2), transparent);
            transition: left 0.5s;
        }
        .badge:hover::before {
            left: 100%;
        }
        .badge:hover {
            background: var(--neon);
            color: var(--bg);
            box-shadow: 0 0 30px rgba(0, 255, 157, 0.5);
            transform: translateY(-3px);
        }
        .badge-alt {
            border-color: var(--neon2);
            color: var(--neon2);
        }
        .badge-alt:hover {
            background: var(--neon2);
            color: var(--bg);
            box-shadow: 0 0 30px rgba(0, 212, 255, 0.5);
        }

        /* ── TERMINAL ── */
        .terminal {
            background: var(--surface);
            border: 1px solid var(--neon);
            border-radius: 6px;
            padding: 18px 22px;
            margin: 20px 0;
            position: relative;
            box-shadow: 0 0 25px rgba(0, 255, 157, 0.08), inset 0 0 25px rgba(0, 255, 157, 0.03);
            overflow: hidden;
        }
        .terminal::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(180deg, rgba(0, 255, 157, 0.03) 0%, transparent 50%);
            pointer-events: none;
        }
        .prompt {
            color: var(--neon);
            font-weight: bold;
        }
        .cmd {
            color: var(--text);
        }
        .output {
            color: var(--text);
            margin-left: 20px;
        }
        .output-highlight {
            color: var(--neon);
        }
        .cursor {
            animation: blink 1s step-end infinite;
        }
        @keyframes blink {
            50% {
                opacity: 0;
            }
        }
        .status-dot {
            display: inline-block;
            width: 10px;
            height: 10px;
            background: var(--neon);
            border-radius: 50%;
            animation: dotPulse 1.5s ease-in-out infinite;
            vertical-align: middle;
            margin-right: 6px;
        }
        @keyframes dotPulse {
            0%,
            100% {
                box-shadow: 0 0 5px var(--neon);
            }
            50% {
                box-shadow: 0 0 25px var(--neon), 0 0 50px var(--neon);
            }
        }

        /* ── SECTION TITLES ── */
        .section-title {
            color: var(--neon);
            font-size: 1.15rem;
            font-weight: bold;
            margin: 40px 0 18px;
            padding: 12px 18px;
            border-left: 4px solid var(--neon);
            background: rgba(0, 255, 157, 0.04);
            display: flex;
            align-items: center;
            gap: 10px;
            letter-spacing: 2px;
            position: relative;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 18px;
            width: 60px;
            height: 1px;
            background: var(--neon);
            animation: titleLine 3s ease-in-out infinite;
        }
        @keyframes titleLine {
            0%,
            100% {
                width: 60px;
            }
            50% {
                width: 150px;
            }
        }
        .section-sub {
            color: var(--neon);
            font-size: 0.75rem;
            opacity: 0.6;
            font-weight: normal;
            letter-spacing: 1px;
        }

        /* ── NAV ── */
        .nav-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            margin: 25px 0;
        }
        .nav-item {
            background: transparent;
            color: var(--neon);
            border: 1.5px solid rgba(0, 255, 157, 0.3);
            padding: 8px 18px;
            border-radius: 2px;
            font-size: 0.8rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            letter-spacing: 1px;
        }
        .nav-item:hover {
            background: var(--neon);
            color: var(--bg);
            border-color: var(--neon);
            box-shadow: 0 0 20px rgba(0, 255, 157, 0.4);
            transform: translateY(-2px);
        }

        /* ── CARDS ── */
        .card {
            background: var(--surface);
            border: 1px solid rgba(0, 255, 157, 0.15);
            border-radius: 6px;
            padding: 20px;
            margin: 15px 0;
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }
        .card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle at center, rgba(0, 255, 157, 0.05) 0%, transparent 60%);
            opacity: 0;
            transition: opacity 0.4s;
        }
        .card:hover::before {
            opacity: 1;
        }
        .card:hover {
            border-color: var(--neon);
            box-shadow: 0 8px 40px rgba(0, 255, 157, 0.12);
            transform: translateY(-4px);
        }
        .card-title {
            color: var(--neon);
            font-size: 1.05rem;
            font-weight: bold;
            margin-bottom: 10px;
            position: relative;
            z-index: 1;
        }
        .card-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin: 10px 0;
            position: relative;
            z-index: 1;
        }
        .card-tag {
            background: rgba(0, 255, 157, 0.06);
            color: var(--neon);
            padding: 5px 12px;
            border-radius: 2px;
            font-size: 0.72rem;
            border: 1px solid rgba(0, 255, 157, 0.2);
            letter-spacing: 0.5px;
        }
        .card-desc {
            color: var(--text);
            font-size: 0.88rem;
            line-height: 1.7;
            position: relative;
            z-index: 1;
        }

        /* ── TECH GRID ── */
        .tech-category {
            color: var(--neon2);
            font-size: 0.85rem;
            font-weight: bold;
            letter-spacing: 1px;
            margin: 18px 0 10px;
            text-align: center;
        }
        .tech-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            margin: 8px 0;
        }
        .tech-item {
            background: var(--surface);
            color: var(--neon);
            border: 1px solid rgba(0, 255, 157, 0.25);
            padding: 10px 20px;
            border-radius: 2px;
            font-size: 0.82rem;
            letter-spacing: 0.5px;
            transition: all 0.3s;
        }
        .tech-item:hover {
            border-color: var(--neon);
            box-shadow: 0 0 20px rgba(0, 255, 157, 0.25);
            transform: translateY(-3px);
            background: rgba(0, 255, 157, 0.05);
        }

        /* ── STATS ── */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 15px;
            margin: 15px 0;
        }
        .stat-card {
            background: var(--surface);
            border: 1px solid rgba(0, 255, 157, 0.15);
            border-radius: 6px;
            padding: 22px 15px;
            text-align: center;
            transition: all 0.3s;
        }
        .stat-card:hover {
            border-color: var(--neon);
            box-shadow: 0 0 25px rgba(0, 255, 157, 0.1);
            transform: translateY(-3px);
        }
        .stat-icon {
            font-size: 2rem;
            margin-bottom: 8px;
        }
        .stat-value {
            color: var(--neon);
            font-size: 1.6rem;
            font-weight: bold;
        }
        .stat-label {
            color: var(--text);
            font-size: 0.75rem;
            margin-top: 4px;
            letter-spacing: 0.5px;
        }

        /* ── TABLE ── */
        .table-wrapper {
            overflow-x: auto;
            margin: 15px 0;
        }
        .achieve-table {
            width: 100%;
            border-collapse: collapse;
        }
        .achieve-table td {
            background: var(--surface);
            border: 1px solid rgba(0, 255, 157, 0.12);
            padding: 18px 15px;
            text-align: center;
            transition: all 0.3s;
            font-size: 0.85rem;
        }
        .achieve-table td:hover {
            border-color: var(--neon);
            background: rgba(0, 255, 157, 0.02);
            transform: scale(1.02);
        }
        .achieve-icon {
            font-size: 1.8rem;
            display: block;
            margin-bottom: 6px;
        }
        .achieve-title {
            color: var(--neon);
            font-weight: bold;
        }
        .achieve-sub {
            color: var(--text);
            font-size: 0.72rem;
            margin-top: 3px;
        }

        /* ── MISSION BOX ── */
        .mission-box {
            background: var(--surface);
            border: 2px solid var(--neon);
            border-radius: 6px;
            padding: 20px;
            margin: 15px 0;
            text-align: center;
            box-shadow: 0 0 30px rgba(0, 255, 157, 0.1), inset 0 0 30px rgba(0, 255, 157, 0.03);
            position: relative;
            overflow: hidden;
        }
        .mission-box::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, transparent, var(--neon), transparent, var(--neon2), transparent);
            background-size: 400% 400%;
            animation: borderGlow 4s linear infinite;
            border-radius: 6px;
            z-index: -1;
        }
        @keyframes borderGlow {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }
        .mission-text {
            color: var(--neon);
            font-family: 'Fira Code', monospace;
            font-size: 0.8rem;
            line-height: 2;
            letter-spacing: 1px;
        }
        .progress-bar {
            width: 100%;
            height: 5px;
            background: rgba(0, 255, 157, 0.08);
            border-radius: 3px;
            overflow: hidden;
            margin: 15px 0;
        }
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, var(--neon), var(--neon2));
            border-radius: 3px;
            animation: progressPulse 3s ease-in-out infinite;
            box-shadow: 0 0 15px var(--neon);
        }
        @keyframes progressPulse {
            0%,
            100% {
                width: 72%;
            }
            50% {
                width: 82%;
            }
        }

        /* ── YAML BLOCK ── */
        .yaml-block {
            background: rgba(0, 255, 157, 0.02);
            border: 1px solid rgba(0, 255, 157, 0.2);
            border-radius: 4px;
            padding: 15px 20px;
            margin: 12px 0;
            color: var(--neon);
            font-size: 0.82rem;
            line-height: 1.8;
            overflow-x: auto;
        }
        .yaml-key {
            color: var(--neon2);
        }

        /* ── FOOTER ── */
        .footer {
            text-align: center;
            padding: 40px 20px;
            border-top: 1px solid rgba(0, 255, 157, 0.1);
            margin-top: 50px;
        }
        .footer-text {
            color: var(--neon);
            font-size: 0.8rem;
            opacity: 0.5;
            letter-spacing: 2px;
        }
        .footer-wave {
            height: 40px;
            background: linear-gradient(180deg, transparent, rgba(0, 255, 157, 0.03) 50%, transparent);
            margin-bottom: 15px;
        }

        /* ── RESPONSIVE ── */
        @media (max-width: 768px) {
            .title-name {
                font-size: 1.8rem;
            }
            .hologram {
                width: 220px;
                height: 220px;
            }
            .holo-ring:nth-child(1) {
                width: 200px;
                height: 200px;
            }
            .holo-ring:nth-child(2) {
                width: 140px;
                height: 140px;
            }
            .holo-ring:nth-child(3) {
                width: 80px;
                height: 80px;
            }
            .cube {
                width: 100px;
                height: 100px;
            }
            .cube-face {
                width: 100px;
                height: 100px;
            }
            .cf {
                transform: translateZ(50px);
            }
            .cb {
                transform: rotateY(180deg) translateZ(50px);
            }
            .cl {
                transform: rotateY(-90deg) translateZ(50px);
            }
            .cr {
                transform: rotateY(90deg) translateZ(50px);
            }
            .ct {
                transform: rotateX(90deg) translateZ(50px);
            }
            .cbo {
                transform: rotateX(-90deg) translateZ(50px);
            }
            .inner-cube {
                width: 60px;
                height: 60px;
            }
            .inner-face {
                width: 60px;
                height: 60px;
            }
            .icf {
                transform: translateZ(30px);
            }
            .icb {
                transform: rotateY(180deg) translateZ(30px);
            }
            .icl {
                transform: rotateY(-90deg) translateZ(30px);
            }
            .icr {
                transform: rotateY(90deg) translateZ(30px);
            }
            .ict {
                transform: rotateX(90deg) translateZ(30px);
            }
            .icbo {
                transform: rotateX(-90deg) translateZ(30px);
            }
            .container {
                padding: 10px;
            }
            .terminal {
                padding: 12px 14px;
                font-size: 0.8rem;
            }
        }
    </style>
</head>
<body>

    <!-- Scanlines -->
    <div class="scanlines"></div>

    <!-- Boot Screen -->
    <div class="boot-screen">
        <div class="boot-text">SYS.BOOT</div>
        <div class="boot-sub">INITIALIZING NEURAL CORES...</div>
        <div class="boot-bar"><div class="boot-bar-fill"></div></div>
        <div class="boot-spinner"></div>
        <div class="boot-welcome">▸ WELCOME, OPERATOR ◂</div>
    </div>

    <!-- Main -->
    <div class="container">

        <!-- Header -->
        <div class="header">
            <div class="hologram">
                <div class="holo-ring"></div>
                <div class="holo-ring"></div>
                <div class="holo-ring"></div>
                <div class="cube-wrapper">
                    <div class="cube">
                        <div class="cube-face cf"></div><div class="cube-face cb"></div>
                        <div class="cube-face cl"></div><div class="cube-face cr"></div>
                        <div class="cube-face ct"></div><div class="cube-face cbo"></div>
                        <div class="inner-cube">
                            <div class="inner-face icf"></div><div class="inner-face icb"></div>
                            <div class="inner-face icl"></div><div class="inner-face icr"></div>
                            <div class="inner-face ict"></div><div class="inner-face icbo"></div>
                        </div>
                    </div>
                </div>
                <div class="particles">
                    <div class="particle p1"></div><div class="particle p2"></div>
                    <div class="particle p3"></div><div class="particle p4"></div>
                    <div class="particle p5"></div><div class="particle p6"></div>
                </div>
            </div>
            <div class="title-name">KARTHIKEYAN S</div>
            <div class="subtitle">AI ENGINEER · GENERATIVE AI · AGENTIC SYSTEMS</div>
            <div class="badges">
                <a href="https://github.com/skarthi369" class="badge">⟡ GITHUB</a>
                <a href="https://linkedin.com/in/karthikeyan-s" class="badge badge-alt">⟡ LINKEDIN</a>
                <a href="mailto:karthikeyan123401@gmail.com" class="badge">⟡ EMAIL</a>
                <span class="badge badge-alt">⟡ CHENNAI, IN</span>
            </div>
        </div>

        <!-- Terminal -->
        <div class="terminal">
            <span class="prompt">root@karthikeyan:~$</span> <span class="cmd">whoami</span><br>
            <span class="output">> B.Tech AI & Data Science | 1+ yr shipping ML/DL/CV/NLP + GenAI</span><br>
            <span class="output">> Published researcher (ICACT 2026) | 3x Hackathon Winner</span><br>
            <span class="output">> Currently: Generative AI Research Intern @ CDAC</span><br>
            <span class="output">> STATUS: <span class="status-dot"></span><span class="output-highlight">ACTIVE</span></span><br>
            <span class="prompt">root@karthikeyan:~$</span> <span class="cursor">█</span>
        </div>

        <!-- Navigation -->
        <div class="nav-grid">
            <a href="#about" class="nav-item">[ABOUT]</a>
            <a href="#mission" class="nav-item">[MISSION]</a>
            <a href="#stack" class="nav-item">[STACK]</a>
            <a href="#projects" class="nav-item">[PROJECTS]</a>
            <a href="#experience" class="nav-item">[EXPERIENCE]</a>
            <a href="#research" class="nav-item">[RESEARCH]</a>
            <a href="#achievements" class="nav-item">[ACHIEVEMENTS]</a>
            <a href="#contact" class="nav-item">[CONTACT]</a>
        </div>

        <!-- About -->
        <div id="about" class="section-title">
            [ ABOUT ] <span class="
