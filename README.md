<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interview Preparation Guide</title>
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background: linear-gradient(to right, #eef2ff, #fce7f3);
      color: #222;
      padding: 20px;
    }

    h1 {
      text-align: center;
      color: #6d28d9;
    }

    .tab-buttons {
      text-align: center;
      margin-bottom: 20px;
    }

    .tab-buttons button {
      padding: 10px 20px;
      margin: 0 5px;
      background: linear-gradient(to right, #9333ea, #ec4899);
      border: none;
      color: white;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.3s;
    }

    .tab-buttons button:hover {
      transform: scale(1.05);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    }

    .tab-content {
      display: none;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 12px rgba(0, 0, 0, 0.1);
      animation: fadeIn 0.4s ease;
    }

    .tab-content.active {
      display: block;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .dropdown {
      border: 1px solid #ddd;
      border-radius: 8px;
      margin: 10px 0;
      overflow: hidden;
    }

    .dropdown summary {
      padding: 12px 15px;
      cursor: pointer;
      font-weight: 600;
      background: linear-gradient(to right, #6366f1, #a855f7);
      color: white;
      list-style: none;
    }

    .dropdown summary::marker {
      display: none;
    }

    .dropdown summary:hover {
      background: linear-gradient(to right, #7c3aed, #ec4899);
    }

    .dropdown p {
      padding: 15px;
      background-color: #faf5ff;
      color: #444;
      border-top: 1px solid #ddd;
      margin: 0;
    }

    .difficulty {
      margin-top: 10px;
      font-size: 14px;
      font-weight: 600;
      color: #7e22ce;
    }
  </style>
</head>
<body>
  <h1>🚀 Interview Preparation Guide</h1>

  <div class="tab-buttons">
    <button onclick="showTab('questions')">🧠 Technical Q&A</button>
    <button onclick="showTab('coding')">💻 Coding Problems</button>
  </div>

  <!-- Technical Questions Tab -->
  <div id="questions" class="tab-content active">
    <h2>Technical Questions (Dropdown Style)</h2>

    <details class="dropdown">
      <summary>📦 What’s the difference between arrays and linked lists?</summary>
      <p>
        Arrays store elements in contiguous memory locations and allow random access.
        Linked lists store elements as nodes connected by pointers, allowing dynamic resizing but slower access.
      </p>
    </details>

    <details class="dropdown">
      <summary>🌳 When to use a Hash Table vs a Binary Search Tree?</summary>
      <p>
        Use a Hash Table for fast lookups and insertions (O(1) average).
        Use a Binary Search Tree when you need sorted data or range queries (O(log n)).
      </p>
    </details>

    <details class="dropdown">
      <summary>⚙️ Explain the CAP Theorem</summary>
      <p>
        CAP Theorem states that a distributed system can only provide two of the following three guarantees:
        Consistency, Availability, and Partition Tolerance — but not all three simultaneously.
      </p>
    </details>

    <details class="dropdown">
      <summary>🧩 How would you detect a cycle in a linked list?</summary>
      <p>
        Use Floyd’s Cycle Detection Algorithm (Tortoise and Hare). Two pointers move at different speeds — if they meet, there’s a cycle.
      </p>
    </details>

    <details class="dropdown">
      <summary>💬 Tell me about a challenging problem you solved.</summary>
      <p>
        Example: Debugged a production issue by tracing memory leaks in Node.js, implemented optimized caching, and reduced response time by 50%.
      </p>
    </details>
  </div>

  <!-- Coding Problems Tab -->
  <div id="coding" class="tab-content">
    <h2>💻 Coding Practice</h2>

    <p class="difficulty">🟢 Easy Level</p>
    <details class="dropdown">
      <summary>🔢 Two Sum</summary>
      <p>
        Given an array and a target sum, return indices of two numbers that add up to the target.  
        <b>Hint:</b> Use a hash map for O(n) time complexity.
      </p>
    </details>

    <details class="dropdown">
      <summary>🔄 Reverse a String</summary>
      <p>
        Convert `"hello"` to `"olleh"`. Use `.split('').reverse().join('')` or loop manually.
      </p>
    </details>

    <p class="difficulty">🟡 Medium Level</p>
    <details class="dropdown">
      <summary>🧠 LRU Cache Implementation</summary>
      <p>
        Use a combination of a doubly linked list and a hash map to store recently used items efficiently.
      </p>
    </details>

    <details class="dropdown">
      <summary>🔗 Clone a Graph</summary>
      <p>
        Use DFS or BFS to create deep copies of each node while avoiding cycles.
      </p>
    </details>

    <p class="difficulty">🔴 Hard Level</p>
    <details class="dropdown">
      <summary>💧 Trapping Rain Water</summary>
      <p>
        Use two-pointer technique to calculate trapped water efficiently in O(n) time.
      </p>
    </details>

    <details class="dropdown">
      <summary>📈 Median of Two Sorted Arrays</summary>
      <p>
        Use binary search across partitions for O(log(min(n, m))) time complexity.
      </p>
    </details>
  </div>

  <script>
    function showTab(tabName) {
      document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
      document.getElementById(tabName).classList.add('active');
    }
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Interview Preparation Guide</title>
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background: linear-gradient(to right, #eef2ff, #fce7f3);
      color: #222;
      padding: 20px;
    }

    h1 {
      text-align: center;
      color: #6d28d9;
    }

    .tab-buttons {
      text-align: center;
      margin-bottom: 20px;
    }

    .tab-buttons button {
      padding: 10px 20px;
      margin: 0 5px;
      background: linear-gradient(to right, #9333ea, #ec4899);
      border: none;
      color: white;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.2s, box-shadow 0.3s;
    }

    .tab-buttons button:hover {
      transform: scale(1.05);
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
    }

    .tab-content {
      display: none;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 12px rgba(0, 0, 0, 0.1);
      animation: fadeIn 0.4s ease;
    }

    .tab-content.active {
      display: block;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .dropdown {
      border: 1px solid #ddd;
      border-radius: 8px;
      margin: 10px 0;
      overflow: hidden;
    }

    .dropdown summary {
      padding: 12px 15px;
      cursor: pointer;
      font-weight: 600;
      background: linear-gradient(to right, #6366f1, #a855f7);
      color: white;
      list-style: none;
    }

    .dropdown summary::marker {
      display: none;
    }

    .dropdown summary:hover {
      background: linear-gradient(to right, #7c3aed, #ec4899);
    }

    .dropdown p {
      padding: 15px;
      background-color: #faf5ff;
      color: #444;
      border-top: 1px solid #ddd;
      margin: 0;
    }

    .difficulty {
      margin-top: 10px;
      font-size: 14px;
      font-weight: 600;
      color: #7e22ce;
    }
  </style>
</head>
<body>
  <h1>🚀 Interview Preparation Guide</h1>

  <div class="tab-buttons">
    <button onclick="showTab('questions')">🧠 Technical Q&A</button>
    <button onclick="showTab('coding')">💻 Coding Problems</button>
  </div>

  <!-- Technical Questions Tab -->
  <div id="questions" class="tab-content active">
    <h2>Technical Questions (Dropdown Style)</h2>

    <details class="dropdown">
      <summary>📦 What’s the difference between arrays and linked lists?</summary>
      <p>
        Arrays store elements in contiguous memory locations and allow random access.
        Linked lists store elements as nodes connected by pointers, allowing dynamic resizing but slower access.
      </p>
    </details>

    <details class="dropdown">
      <summary>🌳 When to use a Hash Table vs a Binary Search Tree?</summary>
      <p>
        Use a Hash Table for fast lookups and insertions (O(1) average).
        Use a Binary Search Tree when you need sorted data or range queries (O(log n)).
      </p>
    </details>

    <details class="dropdown">
      <summary>⚙️ Explain the CAP Theorem</summary>
      <p>
        CAP Theorem states that a distributed system can only provide two of the following three guarantees:
        Consistency, Availability, and Partition Tolerance — but not all three simultaneously.
      </p>
    </details>

    <details class="dropdown">
      <summary>🧩 How would you detect a cycle in a linked list?</summary>
      <p>
        Use Floyd’s Cycle Detection Algorithm (Tortoise and Hare). Two pointers move at different speeds — if they meet, there’s a cycle.
      </p>
    </details>

    <details class="dropdown">
      <summary>💬 Tell me about a challenging problem you solved.</summary>
      <p>
        Example: Debugged a production issue by tracing memory leaks in Node.js, implemented optimized caching, and reduced response time by 50%.
      </p>
    </details>
  </div>

  <!-- Coding Problems Tab -->
  <div id="coding" class="tab-content">
    <h2>💻 Coding Practice</h2>

    <p class="difficulty">🟢 Easy Level</p>
    <details class="dropdown">
      <summary>🔢 Two Sum</summary>
      <p>
        Given an array and a target sum, return indices of two numbers that add up to the target.  
        <b>Hint:</b> Use a hash map for O(n) time complexity.
      </p>
    </details>

    <details class="dropdown">
      <summary>🔄 Reverse a String</summary>
      <p>
        Convert `"hello"` to `"olleh"`. Use `.split('').reverse().join('')` or loop manually.
      </p>
    </details>

    <p class="difficulty">🟡 Medium Level</p>
    <details class="dropdown">
      <summary>🧠 LRU Cache Implementation</summary>
      <p>
        Use a combination of a doubly linked list and a hash map to store recently used items efficiently.
      </p>
    </details>

    <details class="dropdown">
      <summary>🔗 Clone a Graph</summary>
      <p>
        Use DFS or BFS to create deep copies of each node while avoiding cycles.
      </p>
    </details>

    <p class="difficulty">🔴 Hard Level</p>
    <details class="dropdown">
      <summary>💧 Trapping Rain Water</summary>
      <p>
        Use two-pointer technique to calculate trapped water efficiently in O(n) time.
      </p>
    </details>

    <details class="dropdown">
      <summary>📈 Median of Two Sorted Arrays</summary>
      <p>
        Use binary search across partitions for O(log(min(n, m))) time complexity.
      </p>
    </details>
  </div>

  <script>
    function showTab(tabName) {
      document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
      document.getElementById(tabName).classList.add('active');
    }
  </script>
</body>
</html>
