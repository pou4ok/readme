<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<title>TaskFlow — Локальный трекер задач</title>
<style>
    body {font-family: Arial; max-width: 800px; margin: 20px auto; padding: 20px;}
    .task {padding: 10px; margin: 10px 0; border: 1px solid #ddd; border-radius: 8px; display: flex; align-items: center;}
    .completed {text-decoration: line-through; color: #888;}
    .high {background: #ffebee;} .medium {background: #fff3e0;} .low {background: #e8f5e9;}
</style>
</head>
<body>
<h1>TaskFlow — MVP</h1>
<form id="taskForm">
    <input type="text" id="title" placeholder="Название задачи" required>
    <textarea id="desc" placeholder="Описание"></textarea>
    <input type="date" id="deadline" required>
    <select id="priority">
        <option value="high">Высокий</option>
        <option value="medium" selected>Средний</option>
        <option value="low">Низкий</option>
    </select>
    <button type="submit">Добавить задачу</button>
</form>

<div>
    <button onclick="filterTasks('all')">Все</button>
    <button onclick="filterTasks('active')">Активные</button>
    <button onclick="filterTasks('completed')">Выполненные</button>
</div>

<div id="taskList"></div>

<script>
let tasks = JSON.parse(localStorage.getItem('tasks')) || [];
let currentFilter = 'all';

function saveTasks() {
    localStorage.setItem('tasks', JSON.stringify(tasks));
}

function renderTasks() {
    const list = document.getElementById('taskList');
    list.innerHTML = '';
    const filtered = tasks.filter(t => {
        if (currentFilter === 'active') return !t.completed;
        if (currentFilter === 'completed') return t.completed;
        return true;
    });

    filtered.forEach(task => {
        const div = document.createElement('div');
        div.className = `task ${task.priority} ${task.completed ? 'completed' : ''}`;
        div.innerHTML = `
            <input type="checkbox" ${task.completed ? 'checked' : ''} onchange="toggleComplete('${task.id}')">
            <div style="flex:1">
                <strong>${task.title}</strong><br>
                ${task.description}<br>
                <small>Дедлайн: ${task.deadline} | Приоритет: ${task.priority}</small>
            </div>
            <button onclick="editTask('${task.id}')">Редактировать</button>
            <button onclick="deleteTask('${task.id}')">Удалить</button>
        `;
        list.appendChild(div);
    });
}

document.getElementById('taskForm').addEventListener('submit', e => {
    e.preventDefault();
    const newTask = {
        id: Date.now().toString(),
        title: document.getElementById('title').value,
        description: document.getElementById('desc').value,
        deadline: document.getElementById('deadline').value,
        priority: document.getElementById('priority').value,
        completed: false
    };
    tasks.push(newTask);
    saveTasks();
    renderTasks();
    e.target.reset();
});

function toggleComplete(id) {
    const task = tasks.find(t => t.id === id);
    task.completed = !task.completed;
    saveTasks();
    renderTasks();
}

function deleteTask(id) {
    tasks = tasks.filter(t => t.id !== id);
    saveTasks();
    renderTasks();
}

function editTask(id) {
    const task = tasks.find(t => t.id === id);
    const newTitle = prompt('Новое название:', task.title);
    if (newTitle) {
        task.title = newTitle;
        task.description = prompt('Новое описание:', task.description) || task.description;
        task.deadline = prompt('Новый дедлайн (YYYY-MM-DD):', task.deadline) || task.deadline;
        task.priority = prompt('Новый приоритет (high/medium/low):', task.priority) || task.priority;
        saveTasks();
        renderTasks();
    }
}

window.filterTasks = function(filter) {
    currentFilter = filter;
    renderTasks();
};

renderTasks(); // начальная отрисовка
</script>
</body>
</html>