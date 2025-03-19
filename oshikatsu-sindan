<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>推し活診断</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #d0ebff;
            color: #3a3a3a;
            padding: 20px;
        }
        .container {
            background: white;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
            max-width: 400px;
            width: 100%;
        }
        .question {
            margin: 20px 0;
            font-size: 18px;
            font-weight: bold;
        }
        .button {
            padding: 12px 20px;
            margin: 10px;
            font-size: 16px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            background: #a1c4fd;
            color: white;
            transition: 0.3s;
        }
        .button:hover {
            background: #82aaff;
        }
        .result {
            display: none;
            font-size: 20px;
            font-weight: bold;
            margin-top: 20px;
            color: #2c3e50;
        }
        .share-buttons {
            margin-top: 20px;
        }
        .share-button {
            padding: 10px;
            font-size: 14px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin: 5px;
            color: white;
        }
        .twitter {
            background: #1DA1F2;
        }
        .line {
            background: #06C755;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎀 推し活診断 🎀</h1>
        <p>あなたのオタクタイプを診断しよう！</p>
        
        <div id="quiz">
            <div class="question" id="question-text">Q1. あなたの推しは？</div>
            <button class="button" onclick="answer(1)">一人のガチ推し</button>
            <button class="button" onclick="answer(2)">複数推し</button>
        </div>
        
        <div class="result" id="result"></div>
        
        <div class="share-buttons" id="share-buttons" style="display: none;">
            <button class="share-button twitter" onclick="shareTwitter()">Twitterでシェア</button>
            <button class="share-button line" onclick="shareLine()">LINEでシェア</button>
        </div>
    </div>
    
    <script>
        const questions = [
            "あなたの推しは？",
            "推しが異性と絡んだら？",
            "おこづかいで1万円ゲット！何に使う？",
            "最近、推しのイベントに行った？",
            "推しの現場が大事な予定と被った…どうする？",
            "推しに一言伝えられるなら？",
            "推しのグッズ、どれくらい持ってる？",
            "推しが何か炎上しちゃったら？",
            "推しが好きすぎて辛い時、どうする？",
            "推しがもし活動を辞めたら？"
        ];
        
        let index = 0;
        let score1 = 0;
        let score2 = 0;
        
        function answer(choice) {
            if (choice === 1) score1++;
            if (choice === 2) score2++;
            
            index++;
            if (index < questions.length) {
                document.getElementById("question-text").textContent = "Q" + (index + 1) + ". " + questions[index];
            } else {
                showResult();
            }
        }
        
        function showResult() {
            document.getElementById("quiz").style.display = "none";
            let resultText = "";
            
            if (score1 >= 8) resultText = "ガチ勢オタク：推しのためなら全力投球！";
            else if (score1 >= 5) resultText = "現場最優先オタク：イベントが最重要！";
            else if (score2 >= 8) resultText = "冷静オタク：推しを愛しつつ冷静！";
            else if (score2 >= 5) resultText = "ゆる推しオタク：推し活を無理なく楽しむ派！";
            else resultText = "グッズ収集オタク：推しグッズを愛するコレクター！";
            
            document.getElementById("result").textContent = "あなたの診断結果：" + resultText;
            document.getElementById("result").style.display = "block";
            document.getElementById("share-buttons").style.display = "block";
        }
        
        function shareTwitter() {
            const result = document.getElementById("result").textContent;
            const url = encodeURIComponent("https://yourwebsite.com");
            const text = encodeURIComponent(result + "\n\n#推し活診断");
            window.open(`https://twitter.com/intent/tweet?text=${text}&url=${url}`, '_blank');
        }
        
        function shareLine() {
            const result = document.getElementById("result").textContent;
            const url = encodeURIComponent("https://yourwebsite.com");
            const text = encodeURIComponent(result);
            window.open(`https://line.me/R/msg/text/?${text}%20${url}`, '_blank');
        }
    </script>
</body>
</html>
