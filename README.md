# random-
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Game Gọi Tên Ngẫu Nhiên</title>
</head>
<body>
    <h1>Vòng Quay Gọi Tên</h1>
    <textarea id="nameList" rows="5">Nguyễn Văn A\nTrần Thị B\nLê Văn C</textarea>
    <br>
    <button onclick="pickName()">Gọi Tên</button>
    <h2 id="result">---</h2>

    <script>
        function pickName() {
            const text = document.getElementById('nameList').value;
            const names = text.split('\n').filter(name => name.trim() !== '');
            if (names.length === 0) return;
            const randomName = names[Math.floor(Math.random() * names.length)];
            document.getElementById('result').innerText = "Tên được gọi: " + randomName;
        }
    </script>
</body>
</html>

