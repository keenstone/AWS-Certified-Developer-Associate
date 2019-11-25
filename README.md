# AWS Certified Developer Associate
Map:
https://aws.amazon.com/about-aws/global-infrastructure/ карта расположения регионов AWS. Если навести на точку покажет количество Availability Zones. Также есть карта, где расположены Amazon Edge Services https://aws.amazon.com/cloudfront/features/ Это то, что может быть ближе к пользователю: CDN, Lambda и что-то ещё.
Region - польностью независимая сущность в смысле, что содержит все необходимые сервисы и является самодостаточной единицой. AWS Console ограничена выбранным Region.
Availability Zone - существующая внутри Region сущность созданная для устойчивости. Представляет собой датацентр(?)/несколько датацентов соединных с другими AZ low latency links.
AWS CLI - command line interface https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html позволяет выполнять команды управления в консоли. Установил, далее aws configure - указал регион, формат данных + credential (access key+secret access key) ибо  для выполнения команд нужен Programmatic User. Его придется создавать в IAM. Не забываем про ключик --query ... в нотации http://jmespath.org/ Это позволяет парсить json в удобный выходной формат.
AWS SDK - API для выполнения команд. Есть для несколько языков программирования Go, Java, JS и т.д. Пилятся разными командами и могут не предоставлять все актуальные возможности. Также нужен Programmatic User в IAM.
