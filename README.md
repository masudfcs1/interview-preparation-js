# Interview Preparation Guide

<div>
  <button onclick="showTab('questions')">Questions</button>
  <button onclick="showTab('coding')">Coding</button>
</div>

<div id="questions" class="tab-content" style="display:block;">
  <h2>Technical Questions</h2>

  ### Data Structures
  1. Explain the difference between arrays and linked lists.
  2. When would you use a hash table vs a binary search tree?
  3. How does a heap differ from a binary search tree?

  ### Algorithms
  1. Explain time complexity of quicksort in best and worst cases.
  2. How would you detect a cycle in a linked list?
  3. Describe Dijkstra's algorithm and its applications.

  ### System Design
  1. How would you design a URL shortening service?
  2. Explain the CAP theorem and its implications.
  3. What factors would you consider when designing a chat application?

  ### Behavioral
  1. Tell me about a challenging technical problem you solved.
  2. Describe a time you had to work with a difficult teammate.
  3. How do you handle tight deadlines?
</div>

<div id="coding" class="tab-content" style="display:none;">
  <h2>Coding Problems</h2>

  ### Easy Level
  1. Two Sum - Find two numbers that add up to a target
  2. Reverse a string in-place
  3. Validate balanced parentheses

  ### Medium Level
  1. Implement a LRU Cache
  2. Clone a graph with possible cycles
  3. Find the longest palindromic substring

  ### Hard Level
  1. Regular expression matching
  2. Trapping rain water problem
  3. Median of two sorted arrays

  ### Practice Platforms
  - LeetCode
  - HackerRank
  - CodeSignal
  - CodeForces

  ### Tips
  - Always clarify requirements first
  - Talk through your thought process
  - Start with brute force, then optimize
  - Write clean, modular code
  - Don't forget edge cases
</div>

<script>
function showTab(tabName) {
  const tabs = document.getElementsByClassName("tab-content");
  for (let i = 0; i < tabs.length; i++) {
    tabs[i].style.display = "none";
  }
  document.getElementById(tabName).style.display = "block";
}
</script>

<style>
button {
  padding: 10px 20px;
  margin-right: 5px;
  background-color: #f1f1f1;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

button:hover {
  background-color: #ddd;
}

.tab-content {
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-top: 10px;
}
</style>
