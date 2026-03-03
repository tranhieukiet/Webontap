# Webontap
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Web Ôn Tập Lớp</title>
    <style>
        body {
            font-family: Arial;
            background-color: #f4f8fb;
            text-align: center;
            padding: 50px;
        }
        .box {
            background: white;
            padding: 30px;
            border-radius: 10px;
            width: 400px;
            margin: auto;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        input {
            padding: 10px;
            width: 90%;
            margin: 10px 0;
        }
        button {
            padding: 10px 20px;
            background-color: #2d89ef;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background-color: #1b5fbf;
        }
    </style>
</head>
<body>

<div class="box">
    <h2>Vào Phòng Ôn Tập</h2>
    <input type="text" id="name" placeholder="Nhập tên của bạn">
    <br>
    <input type="text" id="room" placeholder="Nhập mã phòng">
    <br>
    <button onclick="joinRoom()">Vào làm bài</button>
</div>

<script>
function joinRoom() {
    let name = document.getElementById("name").value;
    let room = document.getElementById("room").value;

    if(name === "" || room === "") {
        alert("Vui lòng nhập đầy đủ thông tin!");
        return;
    }

    localStorage.setItem("studentName", name);
    localStorage.setItem("roomCode", room);

    alert("Đã vào phòng: " + room + "\nChào " + name);
}
</script>

</body>
</html>
