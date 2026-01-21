<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>💌 Món Quà Tình Yêu Đặc Biệt 💖</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <style>
        @font-face {
            font-family: 'RomanticFont';
            src: url('1000008571.webp') format('woff2');
            font-weight: normal;
            font-style: normal;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'RomanticFont', 'Dancing Script', cursive, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #ff2e63 0%, #ff6b9d 30%, #ff4081 70%, #c2185b 100%);
            color: white;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
            position: relative;
        }
        
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://cdn.pixabay.com/animation/2023/07/31/02/56/02-56-32-207_512.gif');
            opacity: 0.1;
            z-index: -1;
            pointer-events: none;
        }
        
        .floating-hearts {
            position: fixed;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }
        
        .heart {
            position: absolute;
            font-size: 24px;
            color: rgba(255, 255, 255, 0.6);
            animation: floatHeart 15s linear infinite;
        }
        
        .page {
            display: none;
            width: 100%;
            max-width: 500px;
            text-align: center;
            animation: slideInRight 1s ease-out;
            min-height: 80vh;
            position: relative;
            z-index: 1;
            padding: 20px;
            background: rgba(255, 255, 255, 0.08);
            border-radius: 30px;
            backdrop-filter: blur(10px);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .page::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('https://cdn.pixabay.com/animation/2022/10/12/09/48/09-48-47-926_512.gif');
            opacity: 0.03;
            border-radius: 30px;
            z-index: -1;
        }
        
        .active {
            display: block;
            animation: fadeInUp 1s ease-out;
        }
        
        h1 {
            font-size: 3.5rem;
            margin-bottom: 40px;
            text-shadow: 4px 4px 15px rgba(0, 0, 0, 0.5);
            background: linear-gradient(45deg, #ffffff, #ffebee);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: titleGlow 3s infinite alternate;
            line-height: 1.2;
        }
        
        h2 {
            font-size: 2.8rem;
            margin-bottom: 35px;
            text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.4);
            background: linear-gradient(45deg, #ffebee, #ffcdd2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: pulse 2s infinite;
        }
        
        p {
            font-size: 1.8rem;
            margin-bottom: 25px;
            line-height: 1.8;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
            font-weight: 500;
        }
        
        .btn {
            background: linear-gradient(135deg, #ff4081 0%, #ff2e63 50%, #c2185b 100%);
            color: white;
            border: none;
            padding: 22px 45px;
            font-size: 1.8rem;
            border-radius: 60px;
            cursor: pointer;
            margin-top: 35px;
            box-shadow: 0 15px 35px rgba(255, 64, 129, 0.4);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            font-weight: bold;
            letter-spacing: 1.5px;
            position: relative;
            overflow: hidden;
            min-width: 280px;
        }
        
        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: 0.8s;
        }
        
        .btn:hover::before {
            left: 100%;
        }
        
        .btn:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 25px 50px rgba(255, 64, 129, 0.6);
            background: linear-gradient(135deg, #ff2e63 0%, #ff4081 50%, #ff6b9d 100%);
        }
        
        .btn:active {
            transform: translateY(-3px) scale(1.02);
        }
        
        .btn-sparkle {
            position: absolute;
            width: 20px;
            height: 20px;
            background: rgba(255, 255, 255, 0.8);
            border-radius: 50%;
            pointer-events: none;
            animation: sparkle 1s linear infinite;
        }
        
        /* INPUT FIELD */
        .input-container {
            position: relative;
            width: 90%;
            max-width: 400px;
            margin: 40px auto;
        }
        
        .love-input {
            width: 100%;
            padding: 22px 25px;
            font-size: 1.8rem;
            border-radius: 50px;
            border: 4px solid transparent;
            background: linear-gradient(white, white) padding-box,
                        linear-gradient(45deg, #ff4081, #ff2e63, #c2185b) border-box;
            text-align: center;
            outline: none;
            color: #c2185b;
            font-weight: bold;
            box-shadow: 0 10px 30px rgba(255, 64, 129, 0.3);
            transition: all 0.4s ease;
        }
        
        .love-input:focus {
            transform: scale(1.05);
            box-shadow: 0 15px 40px rgba(255, 64, 129, 0.5);
        }
        
        .love-input::placeholder {
            color: #ff80ab;
            font-style: italic;
        }
        
        /* GAME STYLES */
        .game-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 30px 0;
            padding: 20px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 25px;
            backdrop-filter: blur(5px);
        }
        
        .timer {
            font-size: 2.2rem;
            background: linear-gradient(45deg, #ff4081, #ff2e63);
            padding: 12px 25px;
            border-radius: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        
        .score-display {
            font-size: 2.2rem;
            background: linear-gradient(45deg, #4CAF50, #2E7D32);
            padding: 12px 25px;
            border-radius: 20px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        
        .game-board {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-template-rows: repeat(5, 1fr);
            gap: 15px;
            margin: 30px auto;
            max-width: 400px;
        }
        
        .game-cell {
            width: 85px;
            height: 85px;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
            cursor: grab;
            transition: all 0.3s ease;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
            user-select: none;
            position: relative;
            overflow: hidden;
        }
        
        .game-cell::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, transparent 30%, rgba(255, 255, 255, 0.1) 50%, transparent 70%);
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .game-cell:hover::before {
            opacity: 1;
        }
        
        .game-cell:hover {
            transform: scale(1.08) rotate(5deg);
            background: rgba(255, 255, 255, 0.25);
            box-shadow: 0 12px 30px rgba(255, 64, 129, 0.4);
        }
        
        .game-cell.empty {
            background: rgba(255, 255, 255, 0.05);
            cursor: not-allowed;
        }
        
        .game-cell.empty:hover {
            transform: none;
            background: rgba(255, 255, 255, 0.05);
        }
        
        .game-cell.dragging {
            opacity: 0.7;
            cursor: grabbing;
            transform: scale(1.1);
            z-index: 10;
        }
        
        .progress-container {
            width: 100%;
            height: 25px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            margin: 25px 0;
            overflow: hidden;
            box-shadow: inset 0 2px 10px rgba(0, 0, 0, 0.2);
        }
        
        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, #4CAF50, #8BC34A, #CDDC39);
            border-radius: 15px;
            transition: width 0.5s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }
        
        .progress-bar::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent 30%, rgba(255, 255, 255, 0.3) 50%, transparent 70%);
            animation: shimmer 2s infinite;
        }
        
        /* VIDEO PAGE */
        .video-wrapper {
            position: relative;
            width: 100%;
            max-width: 400px;
            margin: 40px auto;
            border-radius: 30px;
            overflow: hidden;
            box-shadow: 0 25px 60px rgba(0, 0, 0, 0.6);
            transform: perspective(1000px) rotateY(-5deg);
            transition: transform 0.5s ease;
        }
        
        .video-wrapper:hover {
            transform: perspective(1000px) rotateY(0deg);
        }
        
        .video-wrapper video {
            width: 100%;
            border-radius: 30px;
            display: block;
            transform: scale(1.02);
        }
        
        .scrolling-text-container {
            width: 100%;
            margin: 50px auto;
            padding: 30px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 25px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            min-height: 200px;
            overflow: hidden;
            position: relative;
        }
        
        .scrolling-text-line {
            font-size: 2rem;
            line-height: 1.6;
            margin-bottom: 20px;
            opacity: 0;
            transform: translateX(-100%);
            animation: textSlideIn 1s forwards;
            white-space: nowrap;
            overflow: hidden;
            text-align: left;
            padding: 10px 0;
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            font-weight: 500;
        }
        
        /* MAGIC FRAME */
        .magic-frame {
            width: 100%;
            height: 350px;
            background: linear-gradient(45deg, 
                rgba(255, 107, 157, 0.9), 
                rgba(255, 64, 129, 0.9), 
                rgba(194, 24, 91, 0.9));
            border-radius: 30px;
            margin: 40px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
            overflow: hidden;
            box-shadow: 0 30px 60px rgba(255, 64, 129, 0.4);
            transform-style: preserve-3d;
            perspective: 1000px;
        }
        
        .magic-frame::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, 
                transparent, 
                rgba(255, 255, 255, 0.3), 
                transparent 30%);
            animation: rotate 4s linear infinite;
        }
        
        .magic-frame::after {
            content: '';
            position: absolute;
            inset: 5px;
            background: linear-gradient(45deg, #ff2e63, #ff6b9d, #ff4081);
            border-radius: 25px;
        }
        
        .magic-content {
            position: relative;
            z-index: 2;
            font-size: 2.5rem;
            text-align: center;
            background: linear-gradient(45deg, #ffffff, #ffebee);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            padding: 20px;
        }
        
        /* GIFT BOX */
        .gift-container {
            position: relative;
            width: 300px;
            height: 300px;
            margin: 50px auto;
            perspective: 1000px;
            cursor: pointer;
        }
        
        .gift-box {
            width: 100%;
            height: 100%;
            position: relative;
            transform-style: preserve-3d;
            transition: transform 1s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .gift-box.open {
            transform: rotateY(180deg) scale(1.3);
        }
        
        .gift-lid, .gift-base {
            position: absolute;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #ff4081 0%, #ff2e63 50%, #c2185b 100%);
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(255, 64, 129, 0.5);
            backface-visibility: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
        }
        
        .gift-lid::before, .gift-base::before {
            content: '';
            position: absolute;
            top: 10px;
            left: 10px;
            right: 10px;
            bottom: 10px;
            border: 3px dashed rgba(255, 255, 255, 0.3);
            border-radius: 15px;
        }
        
        .gift-lid {
            transform: translateZ(50px);
        }
        
        .gift-content {
            position: absolute;
            width: 100%;
            height: 100%;
            background: white;
            border-radius: 20px;
            transform: rotateY(180deg);
            backface-visibility: hidden;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.3);
        }
        
        .gift-content img {
            width: 90%;
            height: 90%;
            object-fit: cover;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }
        
        .floating-text {
            position: absolute;
            font-size: 3.5rem;
            font-weight: bold;
            color: white !important;
            text-shadow: 0 0 20px rgba(255, 64, 129, 0.8),
                         0 0 40px rgba(255, 64, 129, 0.6),
                         0 0 60px rgba(255, 64, 129, 0.4);
            pointer-events: none;
            z-index: 100;
            animation: floatAround 8s linear infinite;
            opacity: 0;
            white-space: nowrap;
        }
        
        /* ANIMATED CLOCK */
        .clock-container {
            width: 200px;
            height: 200px;
            margin: 50px auto;
            position: relative;
        }
        
        .clock-face {
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            position: relative;
            border: 8px solid rgba(255, 255, 255, 0.3);
            box-shadow: 0 0 50px rgba(255, 64, 129, 0.5);
        }
        
        .clock-hand {
            position: absolute;
            background: white;
            transform-origin: bottom center;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(255, 64, 129, 0.8);
        }
        
        .hour-hand {
            width: 8px;
            height: 60px;
            top: 40px;
            left: 96px;
            animation: rotateHour 12s linear infinite;
        }
        
        .minute-hand {
            width: 6px;
            height: 80px;
            top: 20px;
            left: 97px;
            animation: rotateMinute 6s linear infinite;
        }
        
        .second-hand {
            width: 4px;
            height: 90px;
            top: 10px;
            left: 98px;
            animation: rotateSecond 3s linear infinite;
        }
        
        /* FINAL PAGE */
        .secret-container {
            width: 100%;
            max-width: 300px;
            margin: 40px auto;
            position: relative;
            cursor: pointer;
        }
        
        .secret-image {
            width: 100%;
            border-radius: 25px;
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.5);
            transition: all 0.5s ease;
            filter: drop-shadow(0 10px 20px rgba(255, 64, 129, 0.4));
        }
        
        .secret-image:hover {
            transform: scale(1.05) rotate(3deg);
            box-shadow: 0 35px 70px rgba(255, 64, 129, 0.6);
        }
        
        .message-container {
            width: 100%;
            margin: 50px auto;
            padding: 40px;
            background: rgba(0, 0, 0, 0.4);
            border-radius: 30px;
            backdrop-filter: blur(15px);
            border: 2px solid rgba(255, 255, 255, 0.1);
            min-height: 400px;
            text-align: left;
            overflow: hidden;
        }
        
        .message-line {
            font-size: 1.9rem;
            line-height: 1.8;
            margin-bottom: 25px;
            opacity: 0;
            animation: textReveal 0.8s forwards;
            color: #fff;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
            padding-left: 20px;
            border-left: 3px solid rgba(255, 64, 129, 0.5);
        }
        
        .signature {
            text-align: right;
            font-size: 2.2rem;
            margin-top: 40px;
            color: #ffcdd2;
            font-style: italic;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        /* ANIMATED DOG */
        .dog-container {
            width: 150px;
            height: 150px;
            margin: 40px auto;
            position: relative;
            cursor: pointer;
        }
        
        .animated-dog {
            width: 100%;
            height: 100%;
            background: url('https://i.pinimg.com/originals/03/9c/eb/039cebf0d5c6f5b1a5dc0c5c8a0a86e1.gif') no-repeat center;
            background-size: contain;
            animation: bounceDog 2s infinite ease-in-out;
        }
        
        .dog-bubble {
            position: absolute;
            top: -70px;
            left: 50%;
            transform: translateX(-50%);
            background: white;
            color: #333;
            padding: 15px 25px;
            border-radius: 25px;
            font-size: 1.6rem;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            white-space: nowrap;
            animation: bubbleFloat 3s infinite ease-in-out;
        }
        
        .dog-bubble::after {
            content: '';
            position: absolute;
            top: 100%;
            left: 50%;
            transform: translateX(-50%);
            border-width: 15px;
            border-style: solid;
            border-color: white transparent transparent transparent;
        }
        
        /* MODAL */
        .modal {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.9);
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1000;
            opacity: 0;
            visibility: hidden;
            transition: all 0.5s ease;
        }
        
        .modal.active {
            opacity: 1;
            visibility: visible;
        }
        
        .modal-content {
            background: linear-gradient(135deg, #ff2e63, #ff6b9d);
            padding: 40px;
            border-radius: 30px;
            text-align: center;
            max-width: 500px;
            transform: scale(0.8);
            transition: transform 0.5s ease;
            box-shadow: 0 40px 80px rgba(255, 64, 129, 0.6);
        }
        
        .modal.active .modal-content {
            transform: scale(1);
        }
        
        /* ANIMATIONS */
        @keyframes floatHeart {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        @keyframes titleGlow {
            0% {
                text-shadow: 4px 4px 15px rgba(255, 64, 129, 0.5),
                             0 0 30px rgba(255, 64, 129, 0.3);
            }
            100% {
                text-shadow: 4px 4px 25px rgba(255, 64, 129, 0.8),
                             0 0 50px rgba(255, 64, 129, 0.5),
                             0 0 70px rgba(255, 64, 129, 0.3);
            }
        }
        
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        
        @keyframes sparkle {
            0% {
                transform: translate(0, 0) scale(0);
                opacity: 1;
            }
            100% {
                transform: translate(var(--tx), var(--ty)) scale(1);
                opacity: 0;
            }
        }
        
        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes slideInRight {
            from {
                opacity: 0;
                transform: translateX(100px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        @keyframes textSlideIn {
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes floatAround {
            0% {
                transform: translate(0, 0) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            25% {
                transform: translate(100px, -50px) rotate(90deg);
            }
            50% {
                transform: translate(200px, 50px) rotate(180deg);
            }
            75% {
                transform: translate(100px, 150px) rotate(270deg);
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translate(0, 0) rotate(360deg);
                opacity: 0;
            }
        }
        
        @keyframes rotateHour {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes rotateMinute {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes rotateSecond {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        
        @keyframes textReveal {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes bounceDog {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-30px); }
        }
        
        @keyframes bubbleFloat {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(-20px); }
        }
        
        @keyframes heartExplosion {
            0% {
                transform: scale(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: scale(1) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* RESPONSIVE */
        @media (max-width: 768px) {
            h1 { font-size: 2.8rem; }
            h2 { font-size: 2.2rem; }
            p { font-size: 1.6rem; }
            .btn { font-size: 1.6rem; padding: 20px 35px; }
            .game-cell { width: 70px; height: 70px; font-size: 2.8rem; }
            .scrolling-text-line { font-size: 1.7rem; }
            .message-line { font-size: 1.6rem; }
        }
        
        @media (max-width: 480px) {
            .page { padding: 15px; }
            h1 { font-size: 2.2rem; }
            h2 { font-size: 1.8rem; }
            p { font-size: 1.4rem; }
            .btn { font-size: 1.4rem; padding: 18px 30px; min-width: 250px; }
            .game-cell { width: 60px; height: 60px; font-size: 2.2rem; }
            .gift-container { width: 250px; height: 250px; }
        }
    </style>
</head>
<body>
    <!-- Trái tim bay -->
    <div class="floating-hearts" id="floatingHearts"></div>
    
    <!-- Trang 1 -->
    <div id="page1" class="page active">
        <h1>💌 Một món quà dành cho Eiu 🔐</h1>
        <div class="btn" onclick="nextPage(2)">
            👉 Hãy bắt đầu nào, 🙆‍♂️ 👈
        </div>
        <div style="margin-top: 50px; font-size: 1.6rem; color: rgba(255, 255, 255, 0.8);">
            Món quà tình yêu được tạo với tất cả trái tim ❤️
        </div>
    </div>
    
    <!-- Trang 2 -->
    <div id="page2" class="page">
        <h2>Em có yêu Anh không 🤔?</h2>
        <div class="input-container">
            <input type="text" class="love-input" id="answerInput" 
                   placeholder="Nhập câu trả lời từ trái tim em..."
                   onkeypress="checkAnswer(event)">
        </div>
        <div class="modal" id="messageModal">
            <div class="modal-content">
                <img src="buon.jpeg" width="200" style="border-radius: 20px; margin-bottom: 30px;">
                <p style="font-size: 2rem; margin-bottom: 0;">Không chịu đâu 🥲</p>
            </div>
        </div>
    </div>
    
    <!-- Trang 3 - Game -->
    <div id="page3" class="page">
        <h2>Game Xếp Icon Tình Yêu 💖</h2>
        <p>Kéo thả icon vào ô trống, tạo 3 icon giống nhau để +10 điểm</p>
        
        <div class="game-header">
            <div class="timer">
                ⏳ <span id="timeLeft">20</span>s
            </div>
            <div class="score-display">
                💖 <span id="score">0</span>/100
            </div>
        </div>
        
        <div class="progress-container">
            <div id="scoreProgress" class="progress-bar" style="width: 0%"></div>
        </div>
        
        <div class="game-board" id="gameBoard"></div>
        
        <div class="modal" id="timeoutModal">
            <div class="modal-content">
                <img src="linh1.jpeg" width="200" style="border-radius: 20px; margin-bottom: 30px;">
                <p style="font-size: 2.2rem; line-height: 1.5;">
                    Thôi thì cô đẹp quá lên tôi cho qua đó nhá<br>
                    chứ không phải tôi hám sắc đâu 🙄🙄
                </p>
            </div>
        </div>
    </div>
    
    <!-- Trang 4 - Video -->
    <div id="page4" class="page">
        <h2>💖 Khoảnh Khắc Đặc Biệt 💖</h2>
        
        <div class="video-wrapper">
            <video id="myVideo" src="video.mp4" controls 
                   style="width:100%;border-radius:30px;box-shadow:0 25px 60px rgba(0,0,0,.6)"></video>
        </div>
        
        <div class="scrolling-text-container" id="scrollingTextContainer"></div>
        
        <div class="btn" onclick="nextPage(5)" id="magicBtn" style="display: none;">
            Mĩ nữ cầm tay anh nào 🫴🏻
        </div>
    </div>
    
    <!-- Trang 5 - Quà -->
    <div id="page5" class="page">
        <h2>🎁 Món Quà Bí Mật 🎁</h2>
        <p>Hãy mở hộp quà để khám phá điều bất ngờ!</p>
        
        <div class="gift-container" onclick="openGift()">
            <div class="gift-box" id="giftBox">
                <div class="gift-lid">🎁</div>
                <div class="gift-content">
                    <img src="haita.jpeg">
                </div>
            </div>
        </div>
        
        <div id="clockContainer" class="clock-container" style="display: none;">
            <div class="clock-face">
                <div class="clock-hand hour-hand"></div>
                <div class="clock-hand minute-hand"></div>
                <div class="clock-hand second-hand"></div>
            </div>
        </div>
    </div>
    
    <!-- Trang 6 - Tin nhắn -->
    <div id="page6" class="page">
        <h2>✨ Những Lời Từ Trái Tim ✨</h2>
        <p id="instruction">Hãy dùng ảnh này hồ biến hiện ra thứ cất giấu bên trong đó nha!!</p>
        
        <div class="secret-container">
            <img src="linh2.jpeg" class="secret-image" id="secretImg" style="display: none;">
        </div>
        
        <div class="message-container" id="messageContainer" style="display: none;"></div>
        
        <div class="dog-container" id="dogContainer" style="display: none;">
            <div class="dog-bubble">Ấn vào tôi đi mèo con!</div>
            <div class="animated-dog" onclick="goToMess()"></div>
        </div>
    </div>

    <script>
        // ==================== KHỞI TẠO ====================
        let currentPage = 1;
        let score = 0;
        let timeLeft = 20;
        let gameTimer = null;
        let gameActive = true;
        let draggedElement = null;
        
        // Tạo trái tim bay
        function createFloatingHearts() {
            const container = document.getElementById('floatingHearts');
            for (let i = 0; i < 50; i++) {
                const heart = document.createElement('div');
                heart.className = 'heart';
                heart.innerHTML = '❤️';
                heart.style.left = `${Math.random() * 100}%`;
                heart.style.animationDelay = `${Math.random() * 15}s`;
                heart.style.fontSize = `${Math.random() * 20 + 15}px`;
                container.appendChild(heart);
            }
        }
        
        // ==================== CHUYỂN TRANG ====================
        function nextPage(pageNum) {
            const currentPageEl = document.getElementById(`page${currentPage}`);
            currentPageEl.classList.remove('active');
            currentPageEl.style.animation = 'fadeOut 0.8s ease-out';
            
            // Hiệu ứng chuyển trang
            setTimeout(() => {
                currentPage = pageNum;
                const nextPageEl = document.getElementById(`page${currentPage}`);
                nextPageEl.classList.add('active');
                
                // Khởi tạo trang đích
                switch(pageNum) {
                    case 2:
                        initPage2();
                        break;
                    case 3:
                        initGame();
                        break;
                    case 4:
                        initVideoPage();
                        break;
                    case 5:
                        initGiftPage();
                        break;
                    case 6:
                        initFinalPage();
                        break;
                }
            }, 500);
        }
        
        // ==================== TRANG 2 ====================
        function initPage2() {
            const input = document.getElementById('answerInput');
            input.value = '';
            input.focus();
            
            // Thêm hiệu ứng sparkle cho input
            input.addEventListener('focus', () => {
                createSparkles(input);
            });
        }
        
        function checkAnswer(event) {
            if (event.key !== 'Enter') return;
            
            const input = document.getElementById('answerInput');
            const answer = input.value.toLowerCase().trim();
            const positiveAnswers = ["có", "yêu", "yêu nhiều", "yêu lắm", "có yêu", "yes", "love", "đương nhiên", "chắc chắn"];
            const negativeAnswers = ["0", "không", "không yêu", "no", "nope", "never", "đéo", "không thích"];
            
            // Kiểm tra câu trả lời tích cực
            if (positiveAnswers.some(positive => answer.includes(positive))) {
                createSparkles(input, true);
                setTimeout(() => nextPage(3), 1000);
                return;
            }
            
            // Kiểm tra câu trả lời tiêu cực
            if (negativeAnswers.some(negative => answer.includes(negative))) {
                showModal('messageModal');
                input.value = '';
                input.focus();
                return;
            }
            
            // Câu trả lời không rõ ràng
            alert("💖 Hãy trả lời rõ ràng hơn nhé! 💖");
            input.value = '';
            input.focus();
        }
        
        // ==================== TRANG 3 - GAME ====================
        const icons = ['🥰', '🤩', '😘', '😒', '🤭'];
        let gameBoard = [];
        let emptyCells = [];
        
        function initGame() {
            score = 0;
            timeLeft = 20;
            gameActive = true;
            
            document.getElementById('score').textContent = score;
            document.getElementById('timeLeft').textContent = timeLeft;
            document.getElementById('scoreProgress').style.width = '0%';
            
            // Tạo game board
            createGameBoard();
            renderGameBoard();
            
            // Bắt đầu đếm ngược
            startGameTimer();
        }
        
        function createGameBoard() {
            gameBoard = [];
            emptyCells = [];
            
            // Tạo 15 ô (5x3)
            for (let i = 0; i < 15; i++) {
                const icon = Math.random() > 0.2 ? icons[Math.floor(Math.random() * icons.length)] : null;
                gameBoard.push(icon);
                if (icon === null) emptyCells.push(i);
            }
            
            // Đảm bảo có ít nhất 3 ô trống
            while (emptyCells.length < 3) {
                const randomIndex = Math.floor(Math.random() * 15);
                if (gameBoard[randomIndex] !== null) {
                    gameBoard[randomIndex] = null;
                    emptyCells.push(randomIndex);
                }
            }
        }
        
        function renderGameBoard() {
            const board = document.getElementById('gameBoard');
            board.innerHTML = '';
            
            gameBoard.forEach((icon, index) => {
                const cell = document.createElement('div');
                cell.className = `game-cell ${icon ? 'icon' : 'empty'}`;
                cell.dataset.index = index;
                
                if (icon) {
                    cell.textContent = icon;
                    cell.draggable = true;
                    
                    // Drag events
                    cell.addEventListener('dragstart', handleDragStart);
                    cell.addEventListener('dragend', handleDragEnd);
                }
                
                // Drop events
                cell.addEventListener('dragover', handleDragOver);
                cell.addEventListener('drop', handleDrop);
                
                board.appendChild(cell);
            });
        }
        
        function handleDragStart(e) {
            if (!gameActive) return;
            draggedElement = e.target;
            e.target.classList.add('dragging');
            e.dataTransfer.setData('text/plain', e.target.dataset.index);
        }
        
        function handleDragEnd() {
            if (!gameActive) return;
            if (draggedElement) {
                draggedElement.classList.remove('dragging');
                draggedElement = null;
            }
        }
        
        function handleDragOver(e) {
            if (!gameActive) return;
            e.preventDefault();
        }
        
        function handleDrop(e) {
            if (!gameActive) return;
            e.preventDefault();
            
            if (!draggedElement || !e.target.classList.contains('empty')) return;
            
            const fromIndex = parseInt(draggedElement.dataset.index);
            const toIndex = parseInt(e.target.dataset.index);
            
            // Kiểm tra xem ô có liền kề không
            if (!isAdjacent(fromIndex, toIndex)) {
                alert("Chỉ có thể di chuyển vào ô trống liền kề!");
                return;
            }
            
            // Thực hiện di chuyển
            gameBoard[toIndex] = gameBoard[fromIndex];
            gameBoard[fromIndex] = null;
            
            // Cập nhật emptyCells
            emptyCells = gameBoard.reduce((acc, cell, idx) => {
                if (cell === null) acc.push(idx);
                return acc;
            }, []);
            
            // Kiểm tra kết quả
            checkMatches();
            renderGameBoard();
            
            // Kiểm tra nếu đạt 100 điểm
            if (score >= 100) {
                gameActive = false;
                clearInterval(gameTimer);
                setTimeout(() => {
                    alert("🎉 Xuất sắc! Bạn đã đạt 100 điểm! 💖");
                    nextPage(4);
                }, 1000);
            }
        }
        
        function isAdjacent(index1, index2) {
            const row1 = Math.floor(index1 / 3);
            const col1 = index1 % 3;
            const row2 = Math.floor(index2 / 3);
            const col2 = index2 % 3;
            
            return (Math.abs(row1 - row2) === 1 && col1 === col2) ||
                   (Math.abs(col1 - col2) === 1 && row1 === row2);
        }
        
        function checkMatches() {
            let matched = false;
            
            // Kiểm tra hàng ngang
            for (let row = 0; row < 5; row++) {
                for (let col = 0; col < 1; col++) {
                    const idx1 = row * 3 + col;
                    const idx2 = row * 3 + col + 1;
                    const idx3 = row * 3 + col + 2;
                    
                    if (gameBoard[idx1] && gameBoard[idx1] === gameBoard[idx2] && gameBoard[idx1] === gameBoard[idx3]) {
                        score += 10;
                        matched = true;
                        
                        // Xóa các icon đã khớp
                        gameBoard[idx1] = gameBoard[idx2] = gameBoard[idx3] = null;
                        
                        // Thêm icon mới
                        gameBoard[idx1] = icons[Math.floor(Math.random() * icons.length)];
                        gameBoard[idx2] = icons[Math.floor(Math.random() * icons.length)];
                        gameBoard[idx3] = icons[Math.floor(Math.random() * icons.length)];
                    }
                }
            }
            
            // Kiểm tra hàng dọc
            for (let col = 0; col < 3; col++) {
                for (let row = 0; row < 3; row++) {
                    const idx1 = row * 3 + col;
                    const idx2 = (row + 1) * 3 + col;
                    const idx3 = (row + 2) * 3 + col;
                    
                    if (gameBoard[idx1] && gameBoard[idx1] === gameBoard[idx2] && gameBoard[idx1] === gameBoard[idx3]) {
                        score += 10;
                        matched = true;
                        
                        // Xóa các icon đã khớp
                        gameBoard[idx1] = gameBoard[idx2] = gameBoard[idx3] = null;
                        
                        // Thêm icon mới
                        gameBoard[idx1] = icons[Math.floor(Math.random() * icons.length)];
                        gameBoard[idx2] = icons[Math.floor(Math.random() * icons.length)];
                        gameBoard[idx3] = icons[Math.floor(Math.random() * icons.length)];
                    }
                }
            }
            
            // Cập nhật giao diện
            document.getElementById('score').textContent = score;
            document.getElementById('scoreProgress').style.width = `${score}%`;
            
            // Nếu có khớp, kiểm tra tiếp (combo)
            if (matched) {
                setTimeout(checkMatches, 300);
            }
        }
        
        function startGameTimer() {
            gameTimer = setInterval(() => {
                timeLeft--;
                document.getElementById('timeLeft').textContent = timeLeft;
                
                // Hiệu ứng khi sắp hết giờ
                if (timeLeft <= 5) {
                    document.getElementById('timeLeft').style.color = '#ff4081';
                    document.querySelector('.timer').style.animation = 'pulse 0.5s infinite';
                }
                
                if (timeLeft <= 0) {
                    clearInterval(gameTimer);
                    gameActive = false;
                    
                    if (score < 100) {
                        setTimeout(() => {
                            showModal('timeoutModal');
                            setTimeout(() => {
                                hideModal('timeoutModal');
                                nextPage(4);
                            }, 6000);
                        }, 1000);
                    }
                }
            }, 1000);
        }
        
        // ==================== TRANG 4 ====================
        function initVideoPage() {
            const video = document.getElementById('myVideo');
            const textContainer = document.getElementById('scrollingTextContainer');
            const magicBtn = document.getElementById('magicBtn');
            
            video.onended = function() {
                const message = "Đây chắc chắn là người con gái lạnh nhất mà anh từng yêu cũng là cái cô gái mà anh phải tập điên để thích nghi=))";
                
                // Tách thành các dòng
                const lines = message.split(' ');
                let currentLine = '';
                let lineNumber = 0;
                
                textContainer.innerHTML = '';
                
                // Hiển thị từng dòng
                lines.forEach((word, index) => {
                    currentLine += word + ' ';
                    
                    if (currentLine.length > 20 || index === lines.length - 1) {
                        const lineDiv = document.createElement('div');
                        lineDiv.className = 'scrolling-text-line';
                        lineDiv.textContent = currentLine.trim();
                        lineDiv.style.animationDelay = `${lineNumber * 0.8}s`;
                        textContainer.appendChild(lineDiv);
                        
                        currentLine = '';
                        lineNumber++;
                    }
                });
                
                // Hiển thị nút sau khi chữ hiện xong
                setTimeout(() => {
                    magicBtn.style.display = 'inline-block';
                }, lineNumber * 800 + 1000);
            };
        }
        
        // ==================== TRANG 5 ====================
        function initGiftPage() {
            // Khởi tạo sẵn text floating nhưng ẩn
            for (let i = 0; i < 5; i++) {
                const text = document.createElement('div');
                text.className = 'floating-text';
                text.textContent = 'AI ĐÂY TA';
                text.style.animationDelay = `${i * 1}s`;
                document.getElementById('page5').appendChild(text);
            }
        }
        
        function openGift() {
            const giftBox = document.getElementById('giftBox');
            const clockContainer = document.getElementById('clockContainer');
            
            // Mở hộp quà
            giftBox.classList.add('open');
            
            // Hiệu ứng trái tim bay
            createHeartExplosion(100);
            
            // Hiển thị text floating
            const floatingTexts = document.querySelectorAll('.floating-text');
            floatingTexts.forEach((text, index) => {
                setTimeout(() => {
                    text.style.opacity = '1';
                }, index * 200);
            });
            
            // Hiển thị đồng hồ sau 3 giây
            setTimeout(() => {
                clockContainer.style.display = 'block';
                
                // Chuyển trang sau khi đồng hồ quay
                setTimeout(() => {
                    nextPage(6);
                }, 4000);
            }, 3000);
        }
        
        // ==================== TRANG 6 ====================
        function initFinalPage() {
            const instruction = document.getElementById('instruction');
            const secretImg = document.getElementById('secretImg');
            const messageContainer = document.getElementById('messageContainer');
            const dogContainer = document.getElementById('dogContainer');
            
            // Hiển thị ảnh sau 4 giây
            setTimeout(() => {
                instruction.style.display = 'none';
                secretImg.style.display = 'block';
                
                // Thêm hiệu ứng lắc
                secretImg.classList.add('animate__animated', 'animate__wobble');
                
                // Click vào ảnh để hiện tin nhắn
                secretImg.onclick = function() {
                    secretImg.classList.remove('animate__wobble');
                    secretImg.classList.add('animate__zoomOut');
                    
                    setTimeout(() => {
                        secretImg.style.display = 'none';
                        showMessage();
                    }, 500);
                };
            }, 4000);
        }
        
        function showMessage() {
            const messageContainer = document.getElementById('messageContainer');
            const dogContainer = document.getElementById('dogContainer');
            
            const message = `Nãy giờ chắc em cũng thấy vui rồi đúng không anh lấy niềm vui đó là giá tiền phải trả cho 4 đêm thức này. Trước khi yêu em anh có nói là luân làm em vui nhưng tính anh nó gia trưởng ít khi bộc lộ những gì mình muốn làm lên là hành động nó hay đập vào thực tế lắm=)). Anh cũng không được lãng mạn như bao người , anh không cầu kì không tính toán và không bao giờ có từ(bỏ em).Dòng văn này không phải văn nghị luận mà là văn từ trong lơi sâu nhất anh viết ra. MONG EM HIỂU. KÝ TÊN NGƯỜI LÀM: người yêu em 🫶🏻`;
            
            // Tách thành các dòng
            const words = message.split(' ');
            let currentLine = '';
            let lineNumber = 0;
            
            messageContainer.style.display = 'block';
            messageContainer.innerHTML = '';
            
            // Tạo từng dòng
            words.forEach((word, index) => {
                currentLine += word + ' ';
                
                if (currentLine.length > 25 || index === words.length - 1) {
                    const lineDiv = document.createElement('div');
                    lineDiv.className = 'message-line';
                    lineDiv.textContent = currentLine.trim();
                    lineDiv.style.animationDelay = `${lineNumber * 0.5}s`;
                    messageContainer.appendChild(lineDiv);
                    
                    currentLine = '';
                    lineNumber++;
                }
            });
            
            // Thêm chữ ký
            const signature = document.createElement('div');
            signature.className = 'signature';
            signature.textContent = 'KÝ TÊN: người yêu em 🫶🏻';
            signature.style.animationDelay = `${lineNumber * 0.5}s`;
            messageContainer.appendChild(signature);
            
            // Hiển thị con chó sau khi tin nhắn hiện xong
            setTimeout(() => {
                dogContainer.style.display = 'block';
            }, lineNumber * 500 + 2000);
        }
        
        function goToMess() {
            window.open('https://www.facebook.com/share/1GU3zt4Yn7/', '_blank');
        }
        
        // ==================== UTILITY FUNCTIONS ====================
        function showModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.classList.add('active');
        }
        
        function hideModal(modalId) {
            const modal = document.getElementById(modalId);
            modal.classList.remove('active');
        }
        
        function createSparkles(element, isSuccess = false) {
            const rect = element.getBoundingClientRect();
            const colors = isSuccess ? ['#4CAF50', '#8BC34A', '#CDDC39'] : ['#ff4081', '#ff2e63', '#c2185b'];
            
            for (let i = 0; i < 20; i++) {
                const sparkle = document.createElement('div');
                sparkle.className = 'btn-sparkle';
                sparkle.style.left = `${rect.left + rect.width / 2}px`;
                sparkle.style.top = `${rect.top + rect.height / 2}px`;
                sparkle.style.background = colors[Math.floor(Math.random() * colors.length)];
                sparkle.style.setProperty('--tx', `${Math.random() * 200 - 100}px`);
                sparkle.style.setProperty('--ty', `${Math.random() * 200 - 100}px`);
                document.body.appendChild(sparkle);
                
                setTimeout(() => sparkle.remove(), 1000);
            }
        }
        
        function createHeartExplosion(count) {
            const page = document.getElementById('page5');
            
            for (let i = 0; i < count; i++) {
                const heart = document.createElement('div');
                heart.innerHTML = '❤️';
                heart.style.position = 'absolute';
                heart.style.fontSize = `${Math.random() * 30 + 20}px`;
                heart.style.left = '50%';
                heart.style.top = '50%';
                heart.style.transform = 'translate(-50%, -50%) scale(0)';
                heart.style.opacity = '1';
                heart.style.color = '#ff4081';
                heart.style.zIndex = '1000';
                heart.style.animation = `heartExplosion ${Math.random() * 1 + 1}s ease-out forwards`;
                heart.style.animationDelay = `${Math.random() * 0.5}s`;
                
                page.appendChild(heart);
                
                setTimeout(() => heart.remove(), 2000);
            }
        }
        
        // ==================== KHỞI TẠO BAN ĐẦU ====================
        window.onload = function() {
            createFloatingHearts();
            
            // Thêm hiệu ứng cho các nút
            document.querySelectorAll('.btn').forEach(btn => {
                btn.addEventListener('mouseenter', function(e) {
                    const rect = e.target.getBoundingClientRect();
                    createSparkles(e.target);
                });
            });
        };
    </script>
</body>
</html>
