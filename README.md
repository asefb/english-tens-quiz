<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>English Tenses Quiz</title>
  <style>
    body { font-family: Arial; max-width: 600px; margin: auto; padding: 20px; }
    h2 { color: #2c3e50; }
    .question { margin-bottom: 20px; }
    button { padding: 10px 20px; }
  </style>
</head>
<body>

<h2>English Tenses Quiz</h2>

<form id="quizForm">
  <div class="question">
    <label>1. I _____ to the store yesterday. (go)</label><br>
    <input type="radio" name="q1" value="went"> went<br>
    <input type="radio" name="q1" value="go"> go<br>
    <input type="radio" name="q1" value="gone"> gone
  </div>

  <div class="question">
    <label>2. She _____ dinner when I called. (cook)</label><br>
    <input type="radio" name="q2" value="was cooking"> was cooking<br>
    <input type="radio" name="q2" value="cooked"> cooked<br>
    <input type="radio" name="q2" value="cooking"> cooking
  </div>

  <div class="question">
    <label>3. They _____ in New York since 2010. (live)</label><br>
    <input type="radio" name="q3" value="have lived"> have lived<br>
    <input type="radio" name="q3" value="lived"> lived<br>
    <input type="radio" name="q3" value="are living"> are living
  </div>

  <button type="button" onclick="checkAnswers()">Submit</button>
</form>

<p id="result"></p>

<script>
function checkAnswers() {
  let score = 0;
  const answers = {
    q1: "went",
    q2: "was cooking",
    q3: "have lived"
  };
  for (let q in answers) {
    const selected = document.querySelector(`input[name="${q}"]:checked`);
    if (selected && selected.value === answers[q]) {
      score++;
    }
  }
  document.getElementById("result").innerText = "Your score: " + score + "/3";
}
</script>

</body>
</html>
