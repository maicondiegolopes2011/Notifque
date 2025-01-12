<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Notificação de Mensagem</title>
</head>
<body>
    <h1>Notificação de Mensagem</h1>
    <div id="notification"></div>

    <script>
        window.addEventListener('storage', function(event) {
            if (event.key === 'message') {
                const notification = document.getElementById('notification');
                notification.textContent = 'Nova mensagem: ' + event.newValue;
                alert('Você recebeu uma nova mensagem!');
            }
        });
    </script>
    
</body>
</html>
