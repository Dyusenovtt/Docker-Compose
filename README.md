Домашнее задание к занятию 4 «Оркестрация группой Docker контейнеров на примере Docker Compose» Дюсенов Тимур
Задача 1
https://hub.docker.com/repository/docker/dyusenovtt/custom-nginx/general

Задача 2
<img width="974" height="423" alt="image" src="https://github.com/user-attachments/assets/e7ee8d52-1c68-4bcd-a1cb-9fff6f8f298d" />

Задача 3
<img width="974" height="228" alt="image" src="https://github.com/user-attachments/assets/e63efce5-a3d9-4e87-9685-43f104b8f83b" />
Контейнер остановился, потому что процесс Nginx, который работал в режиме daemon off;, получил сигнал SIGINT (прерывание) от комбинации Ctrl+C. Когда вы подключились через docker attach, вы присоединились к основному процессу контейнера (PID 1). Нажатие Ctrl+C отправило сигнал прерывания этому процессу, и Nginx корректно завершил работу, что привело к остановке контейнера.
<img width="974" height="351" alt="image" src="https://github.com/user-attachments/assets/2d75ab37-c6ef-45d1-b84c-78cc43e89165" />
<img width="974" height="574" alt="image" src="https://github.com/user-attachments/assets/c67d3112-2cd4-4a93-b850-574cfa656173" />
<img width="974" height="188" alt="image" src="https://github.com/user-attachments/assets/0f2ff04a-dd4b-47cc-b11a-b467c3b2e6cc" />
После изменения порта Nginx с 80 на 81 внутри контейнера, внешний доступ через хост-порт 8080 перестал работать.Маппинг портов (-p 127.0.0.1:8080:80) жестко привязан к порту 80 контейнера. Изменение порта внутри контейнера разрывает эту связь.
<img width="974" height="132" alt="image" src="https://github.com/user-attachments/assets/92abcf24-c507-4bc2-a32b-e6b5e8c0e667" />

Задача 4
<img width="974" height="338" alt="image" src="https://github.com/user-attachments/assets/05fb3b22-6677-4e8e-a095-3f79edf1d8ab" />
<img width="974" height="530" alt="image" src="https://github.com/user-attachments/assets/44599c0a-082b-473e-8b11-eface013ed67" />


Задача 5
<img width="974" height="324" alt="image" src="https://github.com/user-attachments/assets/24496aba-a6cc-4967-859b-f15296e87a19" />
Docker Compose по умолчанию использует файл compose.yaml (или compose.yml), если он существует. Если его нет, то ищет docker-compose.yaml. Так как compose.yaml существует, он был запущен, а docker-compose.yaml проигнорирован.
<img width="974" height="449" alt="image" src="https://github.com/user-attachments/assets/eb100303-f834-460b-bcdb-29735506a6f2" />
<img width="974" height="578" alt="image" src="https://github.com/user-attachments/assets/24f69e56-63df-491d-9e43-da1185e5c1dd" />
<img width="974" height="720" alt="image" src="https://github.com/user-attachments/assets/8256a938-3201-4c89-a051-bfab1648983b" />
<img width="974" height="592" alt="image" src="https://github.com/user-attachments/assets/c4af5c46-c277-449d-be3c-59eeab0f669c" />
<img width="974" height="512" alt="image" src="https://github.com/user-attachments/assets/10f8fa8e-6e43-4bb4-8444-70d764ac8d8a" />
<img width="974" height="364" alt="image" src="https://github.com/user-attachments/assets/30a2479f-c399-4fdf-865e-44b1913deac0" />








