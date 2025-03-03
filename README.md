# VuHongThuychoxinloidi
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Điều anh muốn nói với em</title>
    <style>
        body {
            background: #F8C8DC; /* Màu hồng pastel */
            text-align: center;
            color: #fff;
            font-family: 'Arial', sans-serif;
        }
        h1 {
            color: #ff3333;
            font-size: 2.5em;
            margin-top: 40px;
        }
        .container {
            display: none;
            opacity: 0;
            transition: opacity 2s ease-in-out;
        }
        .question {
            font-size: 1.8em;
            margin-top: 20%;
            color: #ff3333;
            font-weight: bold;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            padding: 12px 22px;
            font-size: 1.2em;
            margin: 10px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background-color: #ff6699;
            color: white;
            transition: background 0.3s;
        }
        .buttons button:hover {
            background-color: #ff3366;
        }
        .message-box {
            background: rgba(0, 0, 0, 0.7);
            padding: 25px;
            border-radius: 10px;
            display: inline-block;
            text-align: center;
            max-width: 650px;
            margin-top: 20px;
            font-size: 1.3em;
        }
        .countdown {
            font-size: 1.3em;
            font-weight: bold;
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div id="question-container">
        <p class="question">Cho anh xin lỗi nha!!!</p>
        <div class="buttons">
            <button onclick="showMessage()">Dạ</button>
            <button onclick="alert('Vậy anh sẽ đợi đến khi em đồng ý! 😢')">CC</button>
           </div>
    </div>
    
    <div id="message-container" class="container">
        <h1>Điều anh muốn nói với em</h1>
        <div class="message-box">
            <p>Em à, anh biết mình đã sai, và anh thực sự xin lỗi...</p>
            <p>Không có em, mọi thứ trở nên vô nghĩa. Anh mong được nhìn thấy nụ cười của em một lần nữa.</p>
            <p>Thời gian không thể quay lại, nhưng tình yêu anh dành cho em là mãi mãi.</p>
            <div class="countdown" id="countdown"></div>
        </div>
    </div>

    <script>
        function showMessage() {
            document.getElementById('question-container').style.display = 'none';
            const messageContainer = document.getElementById('message-container');
            messageContainer.style.display = 'block';
            setTimeout(() => { messageContainer.style.opacity = 1; }, 100);
            updateCountdown();
            setInterval(updateCountdown, 1000);
        }
        function updateCountdown() {
            const startDate = new Date('2023-01-22T00:00:00'); 
            const now = new Date();
            const diff = Math.floor((now - startDate) / 1000);
            const days = Math.floor(diff / (60 * 60 * 24));
            const hours = Math.floor((diff % (60 * 60 * 24)) / (60 * 60));
            const minutes = Math.floor((diff % (60 * 60)) / 60);
            const seconds = diff % 60;
            document.getElementById('countdown').innerText = `Đã ${days} ngày, ${hours} giờ, ${minutes} phút, ${seconds} giây kể từ khi anh yêu em.`;
        }
    </script>
</body>
</html>

