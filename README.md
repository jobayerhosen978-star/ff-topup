<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FF Diamond Top Up</title>
<style>
    body {
        font-family: Arial;
        background: #f0f0f0;
        padding: 20px;
    }
    .container {
        max-width: 380px;
        margin: auto;
        background: #fff;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 0 10px #999;
    }
    input, select {
        width: 100%;
        padding: 10px;
        margin: 8px 0;
        border-radius: 8px;
        border: 1px solid #aaa;
    }
    button {
        width: 100%;
        padding: 12px;
        background: #25D366;
        color: white;
        border: none;
        border-radius: 8px;
        font-size: 16px;
        cursor: pointer;
    }
    button:hover {
        background: #1eb15a;
    }
</style>
</head>
<body>

<div class="container">
    <h2>💎 Free Fire Diamond Top-Up</h2>

    <label>Player ID</label>
    <input type="text" id="playerId" placeholder="Enter your FF ID">

    <label>WhatsApp Number</label>
    <input type="text" id="whatsapp" placeholder="88017XXXXXXXX">

    <label>Select Diamond Package</label>
    <select id="package">
        <option value="">Select Package</option>
        <option value="100 Diamonds - 90৳">100 Diamonds - 90৳</option>
        <option value="210 Diamonds - 190৳">210 Diamonds - 190৳</option>
        <option value="500 Diamonds - 450৳">500 Diamonds - 450৳</option>
        <option value="1000 Diamonds - 850৳">1000 Diamonds - 850৳</option>
    </select>

    <button onclick="placeOrder()">Order Now</button>
</div>

<script>
function placeOrder() {
    const playerId = document.getElementById("playerId").value;
    const whatsapp = document.getElementById("whatsapp").value;
    const pkg = document.getElementById("package").value;

    if (!playerId || !whatsapp || !pkg) {
        alert("Please fill all fields!");
        return;
    }

    // YOUR ADMIN WHATSAPP NUMBER HERE 👇
    const adminNumber = "8801906000314";  

    const msg = `Hello, I want to buy:\n\nPlayer ID: ${playerId}\nPackage: ${pkg}\nMy WhatsApp: ${whatsapp}`;

    const url = `https://wa.me/${adminNumber}?text=${encodeURIComponent(msg)}`;
    window.open(url, "_blank");
}
</script>

</body>
</html>
