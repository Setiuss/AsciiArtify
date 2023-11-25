
### Створення нового додатку в розгорнутому Argo CD на k3d

## Demo
![Demo](/.data/argo_demo.gif)

** Додаємо новий додаток з репозиторію **
`https://github.com/den-vasyliev/go-demo-app`

- задаємо ім'я demo
- обираємо проєкт default
- в опціях синхронізації зазначаємо auto-create namespace
- задаэмо посилання на ресурс go-demo-app
- залишаємо ревізію HEAD
- після завантаженні інформації з ресурсу, обираємо шлях Helm
- обираємо посилання на кластер https://kubernetes.default.svc
- вказуємо простір імен argocd
- натискаэмо кнопку створити (create)