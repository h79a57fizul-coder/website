<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Micro Job BD</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; background-color: #f4f4f9; padding-bottom: 60px; }
        header { background: #2c3e50; color: white; padding: 15px; text-align: center; }
        .balance-card { background: white; margin: 10px; padding: 15px; border-radius: 10px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); text-align: center; }
        .job-card { background: white; margin: 10px; padding: 15px; border-radius: 8px; border-left: 5px solid #27ae60; }
        .footer-menu { position: fixed; bottom: 0; width: 100%; background: white; display: flex; justify-content: space-around; padding: 10px; border-top: 1px solid #ddd; }
        .btn { background: #27ae60; color: white; padding: 8px 15px; border: none; border-radius: 5px; cursor: pointer; }
        #upload-section, #profile-section { display: none; padding: 20px; }
        input, textarea { width: 100%; padding: 10px; margin: 10px 0; border: 1px solid #ddd; }
    </style>
</head>
<body>

<header><h2>Micro Job Platform</h2></header>

<div class="balance-card">
    <p>ব্যালেন্স: <b>$0.00</b> | <span style="color:orange;">পেন্ডিং: $0.00</span></p>
</div>

<div id="home-page">
    <div class="job-card">
        <h3>ইউটিউব সাবস্ক্রাইব</h3>
        <p>পেমেন্ট: $0.05</p>
        <button class="btn" onclick="alert('বিস্তারিত: লিঙ্ক ওপেন করুন ও কাজ শেষে ২টা স্ক্রিনশট দিন।')">বিস্তারিত</button>
    </div>
</div>

<div id="upload-section">
    <h3>নতুন কাজ আপলোড দিন</h3>
    <input type="text" placeholder="কাজের নাম">
    <input type="number" placeholder="কাজের মূল্য">
    <textarea placeholder="কাজের বিস্তারিত লিখুন..."></textarea>
    <p>কাজের স্ক্রিনশট বা ছবি দিন:</p>
    <input type="file">
    <button class="btn">কাজ আপলোড করুন</button>
</div>

<div id="profile-section">
    <h3>আমার প্রোফাইল</h3>
    <p>মোট আয়: $0.00</p>
    <button class="btn" style="background: #3498db;" onclick="alert('উইথড্র করার জন্য নূন্যতম $৫ প্রয়োজন')">উইথড্র (Withdraw)</button>
</div>

<div class="footer-menu">
    <div onclick="showHome()">🏠 হোম</div>
    <div onclick="showUpload()">➕ কাজ দিন</div>
    <div onclick="showProfile()">👤 প্রোফাইল</div>
</div>

<script>
    function showHome() {
        document.getElementById('home-page').style.display = 'block';
        document.getElementById('upload-section').style.display = 'none';
        document.getElementById('profile-section').style.display = 'none';
    }
    function showUpload() {
        document.getElementById('home-page').style.display = 'none';
        document.getElementById('upload-section').style.display = 'block';
        document.getElementById('profile-section').style.display = 'none';
    }
    function showProfile() {
        document.getElementById('home-page').style.display = 'none';
        document.getElementById('upload-section').style.display = 'none';
        document.getElementById('profile-section').style.display = 'block';
    }
</script>

</body>
</html>
