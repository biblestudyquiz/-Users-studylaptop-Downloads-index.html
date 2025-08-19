<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>John Chapter 1 Quiz</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin: 20px; }
    .quiz-container { max-width: 800px; margin: auto; background: #fff; padding: 20px; border-radius: 12px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); }
    h1 { text-align: center; }
    .question { margin-bottom: 20px; }
    .options label { display: block; margin-bottom: 6px; }
    button { background: #4CAF50; color: white; border: none; padding: 10px 20px; border-radius: 6px; cursor: pointer; }
    button:hover { background: #45a049; }
    #results { margin-top: 20px; font-weight: bold; text-align: center; }
  </style>
</head>
<body>
  <div class="quiz-container">
    <h1>John Chapter 1 Quiz</h1>
    <form id="quizForm">
      <div class="question">
        <p>1) What does John mean when he calls Jesus “the Word” (Logos) in verse 1?</p>
        <div class="options">
          <label><input type="radio" name="q1" value="A"> A) Jesus was a wise teacher who explained the Jewish law.</label>
          <label><input type="radio" name="q1" value="B"> B) Jesus is God in human form, revealing who God truly is.</label>
          <label><input type="radio" name="q1" value="C"> C) Jesus is a prophet who delivered God’s commands.</label>
          <label><input type="radio" name="q1" value="D"> D) Jesus was the first book of the Bible.</label>
        </div>
      </div>

      <div class="question">
        <p>2) How long was Jesus’s ministry according to John’s Gospel?</p>
        <div class="options">
          <label><input type="radio" name="q2" value="A"> A) About 1 year</label>
          <label><input type="radio" name="q2" value="B"> B) About 2 years</label>
          <label><input type="radio" name="q2" value="C"> C) About 3 years</label>
          <label><input type="radio" name="q2" value="D"> D) About 4 years</label>
        </div>
      </div>

      <div class="question">
        <p>3) Which best explains John 1:3, “Without Him nothing was made that has been made”?</p>
        <div class="options">
          <label><input type="radio" name="q3" value="A"> A) Jesus was present at creation, but not involved in it.</label>
          <label><input type="radio" name="q3" value="B"> B) Jesus was created first, and then He created everything else.</label>
          <label><input type="radio" name="q3" value="C"> C) Jesus was the active Creator; nothing exists apart from Him.</label>
          <label><input type="radio" name="q3" value="D"> D) Jesus only created spiritual life, not the physical world.</label>
        </div>
      </div>

      <div class="question">
        <p>4) Who was John the Baptist compared to in prophecy?</p>
        <div class="options">
          <label><input type="radio" name="q4" value="A"> A) Moses</label>
          <label><input type="radio" name="q4" value="B"> B) Elijah</label>
          <label><input type="radio" name="q4" value="C"> C) Isaiah</label>
          <label><input type="radio" name="q4" value="D"> D) Abraham</label>
        </div>
      </div>

      <div class="question">
        <p>5) Why did John the Baptist call Jesus “the Lamb of God”?</p>
        <div class="options">
          <label><input type="radio" name="q5" value="A"> A) Because lambs were gentle, like Jesus.</label>
          <label><input type="radio" name="q5" value="B"> B) Because Jesus would be the final sacrifice for sin.</label>
          <label><input type="radio" name="q5" value="C"> C) Because Jesus was born in a stable with lambs.</label>
          <label><input type="radio" name="q5" value="D"> D) Because the Jews worshiped lambs during Passover.</label>
        </div>
      </div>

      <div class="question">
        <p>6) What name did Jesus give Simon when they first met?</p>
        <div class="options">
          <label><input type="radio" name="q6" value="A"> A) James</label>
          <label><input type="radio" name="q6" value="B"> B) Cephas (Peter)</label>
          <label><input type="radio" name="q6" value="C"> C) Andrew</label>
          <label><input type="radio" name="q6" value="D"> D) Bartholomew</label>
        </div>
      </div>

      <div class="question">
        <p>7) Why did people doubt Jesus could be the Messiah when Philip said He was from Nazareth?</p>
        <div class="options">
          <label><input type="radio" name="q7" value="A"> A) Because Nazareth was considered unimportant and despised.</label>
          <label><input type="radio" name="q7" value="B"> B) Because Nazareth was a wealthy city full of Romans.</label>
          <label><input type="radio" name="q7" value="C"> C) Because the Messiah was supposed to come from Egypt.</label>
          <label><input type="radio" name="q7" value="D"> D) Because Nazareth had no synagogues at that time.</label>
        </div>
      </div>

      <div class="question">
        <p>8) Which of the following is <strong>not</strong> one of the eight names for Jesus in John 1?</p>
        <div class="options">
          <label><input type="radio" name="q8" value="A"> A) Rabbi</label>
          <label><input type="radio" name="q8" value="B"> B) King of Israel</label>
          <label><input type="radio" name="q8" value="C"> C) Son of David</label>
          <label><input type="radio" name="q8" value="D"> D) Lamb of God</label>
        </div>
      </div>

      <button type="button" onclick="gradeQuiz()">Submit Answers</button>
    </form>
    <div id="results"></div>
  </div>

  <script>
    function gradeQuiz() {
      const correctAnswers = {
        q1: 'B',
        q2: 'C',
        q3: 'C',
        q4: 'B',
        q5: 'B',
        q6: 'B',
        q7: 'A',
        q8: 'C'
      };
      let score = 0;
      const form = document.forms['quizForm'];
      const total = Object.keys(correctAnswers).length;

      for (let key in correctAnswers) {
        const answer = form[key].value;
        if (answer === correctAnswers[key]) {
          score++;
        }
      }

      const percentage = Math.round((score / total) * 100);
      document.getElementById('results').innerHTML = `You scored ${score} out of ${total} (${percentage}%). Try again for a perfect score!`;
    }
  </script>
</body>
</html>
