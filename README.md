# Interview Preparation Guide

<div class="tabs">
  <button class="tab-button active" onclick="openTab('questions')">Questions</button>
  <button class="tab-button" onclick="openTab('coding')">Coding</button>
</div>

<div id="questions" class="tab-content" style="display:block;">
  <h2>Technical Questions</h2>
  
  <div class="question-container">
    <div class="question" onclick="toggleAnswer(1)">
      <h3>1. What is the difference between let, const, and var in JavaScript?</h3>
      <div class="answer" id="answer1">
        <p><strong>var:</strong> Function-scoped, can be redeclared and updated, hoisted</p>
        <p><strong>let:</strong> Block-scoped, can be updated but not redeclared, not hoisted</p>
        <p><strong>const:</strong> Block-scoped, cannot be updated or redeclared, must be initialized during declaration</p>
      </div>
    </div>

    <div class="question" onclick="toggleAnswer(2)">
      <h3>2. Explain the concept of closures in JavaScript.</h3>
      <div class="answer" id="answer2">
        <p>A closure is a function that has access to its own scope, the outer function's variables, and global variables - even after the outer function has returned. This is possible because JavaScript functions form closures when they are created.</p>
        <p>Example:</p>
        <pre>function outer() {
  let count = 0;
  return function inner() {
    count++;
    return count;
  }
}</pre>
      </div>
    </div>

    <div class="question" onclick="toggleAnswer(3)">
      <h3>3. What is the Virtual DOM in React?</h3>
      <div class="answer" id="answer3">
        <p>The Virtual DOM is a lightweight copy of the actual DOM that React maintains in memory. When state changes occur, React:</p>
        <ol>
          <li>Creates a new Virtual DOM representation</li>
          <li>Compares it with the previous one (diffing)</li>
          <li>Updates only the changed parts in the real DOM (reconciliation)</li>
        </ol>
        <p>This makes React updates more efficient than direct DOM manipulation.</p>
      </div>
    </div>
  </div>
</div>

<div id="coding" class="tab-content">
  <h2>Coding Challenges</h2>
  
  <div class="question-container">
    <div class="question" onclick="toggleAnswer(4)">
      <h3>1. Reverse a string</h3>
      <div class="answer" id="answer4">
        <p><strong>Solution:</strong></p>
        <pre>function reverseString(str) {
  return str.split('').reverse().join('');
}

// ES6
const reverseString = str => [...str].reverse().join('');</pre>
      </div>
    </div>

    <div class="question" onclick="toggleAnswer(5)">
      <h3>2. Find the factorial of a number</h3>
      <div class="answer" id="answer5">
        <p><strong>Solution (recursive):</strong></p>
        <pre>function factorial(n) {
  if (n === 0 || n === 1) return 1;
  return n * factorial(n - 1);
}</pre>
        <p><strong>Solution (iterative):</strong></p>
        <pre>function factorial(n) {
  let result = 1;
  for (let i = 2; i <= n; i++) {
    result *= i;
  }
  return result;
}</pre>
      </div>
    </div>

    <div class="question" onclick="toggleAnswer(6)">
      <h3>3. Implement a debounce function</h3>
      <div class="answer" id="answer6">
        <p><strong>Solution:</strong></p>
        <pre>function debounce(func, delay) {
  let timeoutId;
  return function(...args) {
    clearTimeout(timeoutId);
    timeoutId = setTimeout(() => {
      func.apply(this, args);
    }, delay);
  };
}</pre>
      </div>
    </div>
  </div>
</div>

<style>
  .tabs {
    margin-bottom: 20px;
    border-bottom: 1px solid #ddd;
  }
  
  .tab-button {
    padding: 10px 20px;
    background: #f1f1f1;
    border: none;
    cursor: pointer;
    font-size: 16px;
  }
  
  .tab-button.active {
    background: #4CAF50;
    color: white;
  }
  
  .tab-content {
    display: none;
    padding: 20px;
    border: 1px solid #ddd;
    border-top: none;
  }
  
  .question {
    padding: 15px;
    margin: 10px 0;
    background: #f9f9f9;
    border-left: 4px solid #4CAF50;
    cursor: pointer;
  }
  
  .question:hover {
    background: #f1f1f1;
  }
  
  .answer {
    display: none;
    padding: 15px;
    margin-top: 10px;
    background: white;
    border: 1px solid #ddd;
  }
  
  pre {
    background: #f5f5f5;
    padding: 10px;
    border-radius: 4px;
    overflow-x: auto;
  }
</style>

<script>
  function openTab(tabName) {
    const tabContents = document.getElementsByClassName('tab-content');
    for (let i = 0; i < tabContents.length; i++) {
      tabContents[i].style.display = 'none';
    }
    
    const tabButtons = document.getElementsByClassName('tab-button');
    for (let i = 0; i < tabButtons.length; i++) {
      tabButtons[i].className = tabButtons[i].className.replace(' active', '');
    }
    
    document.getElementById(tabName).style.display = 'block';
    event.currentTarget.className += ' active';
  }
  
  function toggleAnswer(id) {
    const answer = document.getElementById(`answer${id}`);
    answer.style.display = answer.style.display === 'block' ? 'none' : 'block';
  }
</script>
