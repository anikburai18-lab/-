<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shubho Mahalaya Greeting</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background-color: #4a000b;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            color: #fff;
        }

        .card {
            background-color: #800016;
            border: 2px solid #ffd700;
            border-radius: 15px;
            padding: 30px 20px;
            width: 320px;
            text-align: center;
            box-shadow: 0 10px 25px rgba(0,0,0,0.5);
            margin: 20px;
        }

        h1 {
            color: #ffd700;
            font-size: 22px;
            margin-bottom: 15px;
        }

        p {
            font-size: 15px;
            line-height: 1.6;
            color: #fff8e7;
            margin-bottom: 15px;
        }

        .input-box {
            width: 85%;
            padding: 10px;
            border: 1px solid #ffd700;
            border-radius: 8px;
            outline: none;
            font-size: 14px;
            text-align: center;
            margin-bottom: 20px;
            background-color: #fff8e7;
            color: #4a000b;
            font-weight: bold;
        }

        .btn {
            background-color: #ffd700;
            color: #800016;
            border: none;
            padding: 10px 25px;
            font-size: 15px;
            font-weight: bold;
            border-radius: 20px;
            cursor: pointer;
            transition: background 0.3s;
        }

        .btn:hover {
            background-color: #fff;
        }

        /* Page Toggle Setup */
        #page1 {
            display: block;
        }

        #page2 {
            display: none;
            animation: fadeIn 0.6s ease-in-out;
        }

        .durga-svg {
            width: 100px;
            height: 100px;
            margin: 15px 0;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: scale(0.95); }
            to { opacity: 1; transform: scale(1); }
        }

        .user-name {
            color: #ffd700;
            font-weight: bold;
            font-size: 18px;
        }
    </style>
</head>
<body>

    <div class="card">
        <!-- 1ST PAGE: NAME INPUT -->
        <div id="page1">
            <h1>🌼 শুভ মহালয়া 🌼</h1>
            <p>আগমণীর সুরে ভরে উঠুক চতুর্দিক!</p>
            <input type="text" id="nameInput" class="input-box" placeholder="আপনার নাম লিখুন..." />
            <br>
            <button class="btn" onclick="openGreeting()">কার্ড খুলুন ✨</button>
        </div>

        <!-- 2ND PAGE: GREETING & DURGA IMAGE -->
        <div id="page2">
            <h1>🌼 শুভ মহালয়া 🌼</h1>
            
            <!-- Maa Durga Icon SVG -->
            <svg class="durga-svg" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
                <circle cx="50" cy="50" r="45" fill="#FFF8E7" stroke="#FFD700" stroke-width="3"/>
                <!-- Third Eye / Trishul Symbol Representation -->
                <path d="M50 25 C45 35 45 45 50 55 C55 45 55 35 50 25 Z" fill="#800016"/>
                <circle cx="50" cy="38" r="3" fill="#FFD700"/>
                <!-- Eyes -->
                <path d="M30 48 Q40 40 50 48 Q40 55 30 48 Z" fill="#800016"/>
                <circle cx="40" cy="47" r="2" fill="#FFF"/>
                <path d="M70 48 Q60 40 50 48 Q60 55 70 48 Z" fill="#800016"/>
                <circle cx="60" cy="47" r="2" fill="#FFF"/>
                <!-- Bindi -->
                <circle cx="50" cy="43" r="4" fill="#D32F2F"/>
                <!-- Smile -->
                <path d="M42 62 Q50 68 58 62" stroke="#800016" stroke-width="2" stroke-linecap="round" fill="none"/>
            </svg>

            <p>প্রিয় <span id="displayName" class="user-name"></span>,</p>
            <p>আপনাকে ও আপনার সমগ্র পরিবারকে শুভ মহালয়ার প্রীতি ও আন্তরিক শুভেচ্ছা। মহালয়ার এই পূণ্য লগ্নে মা দুর্গার আগমনে আপনার জীবন আলো ও আনন্দে ভরে উঠুক।</p>
            
            <button class="btn" style="margin-top:15px;" onclick="goBack()">আবার দেখুন 🔄</button>
        </div>
    </div>

    <script>
        function openGreeting() {
            var name = document.getElementById("nameInput").value.trim();

            if (name === "") {
                alert("অনুগ্রহ করে আপনার নাম লিখুন!");
                return;
            }

            document.getElementById("displayName").textContent = name;
            document.getElementById("page1").style.display = "none";
            document.getElementById("page2").style.display = "block";
        }

        function goBack() {
            document.getElementById("page1").style.display = "block";
            document.getElementById("page2").style.display = "none";
            document.getElementById("nameInput").value = "";
        }
    </script>

</body>
</html>
