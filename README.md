# to-do-list-JAVASCRIPT-
Javascript 
<!DOCTYPE html>
<html>
<body>

<h1>To-Do List</h1>

<input type="text" id="new-todo" placeholder="Enter new to-do">
<button onclick="addTodo()">Add</button>

<ul id="todo-list"></ul>

<script>
  const todoList = document.getElementById('todo-list');
  const newTodoInput = document.getElementById('new-todo');

  let todos = []; // This array will store our to-do items

  function addTodo() {
    const newTodoText = newTodoInput.value;
    if (newTodoText) {
      todos.push(newTodoText);
      newTodoInput.value = ""; // Clear the input field
      displayTodos();
    }
  }

  function displayTodos() {
    todoList.innerHTML = ""; // Clear the list before adding new items
    for (const todo of todos) {
      const listItem = document.createElement('li');
      listItem.innerText = todo;
      todoList.appendChild(listItem);
    }
  }
</script>

</body>
</html>
