Identity Access Management https://docs.aws.amazon.com/iam/index.html - сервис для аутентификации, авторизации и управления доступностью AWS сервисов. Един для всех сервисов. 
Реплицируется по всем регионам и доступен всюду.  В дополнение к Web console, SDK, CLI имеет свой IAM HTTPS API

IAM Components:
  Identities
    Users
    Groups
    Roles
  Policies
  Identity Providers
  
User  - сущность у которой есть имя. Не обязательно конкретный пользователь. Может быть пользователь для CLI. Бывает 2-х видов или их сочетание:
  1. Programmatic Access - для работы под этой учеткой нужны пара Access Key + Secret Access Key и он нужен для работы из CLI или SDK
  2. AWS Management Console Access - это для доступа к console.aws.amazon.com
  Есть понятие Root User это основной пользователь, который имеет всюду доступ и может все. Под ним не работаем))) Создали Root учетку, 
  создали специального пользователя и под ним делаем дела. 

Group - группа состоит из пользователей и имеет имя. Имя лучше не менять. Меняется его идентификатор и это равнозначно созданию новой 
группы.

Policies - сущность представляющая собой набор прав (set of permissions) и может быть назначена пользователю или группе (каждому полььзователю в группе).
  содержит 4 свойства:
  1 Effect - разрешено или запрещено
  2 Action - что разрешено/запрещено. Может быть специфично для выборанного ресурса
  3 Resource - над чем можно/нельзя
  4 Condition - 
  их можно копировать или создавать свои с нуля.
  Policies выданные на группу могут быть переопределны Policies выданными пользователю.

Roles - сущность с назначенными ей правами. Может быть выдана кому-угодно/чему угодно, если такое нужно. Например, можно назначить роль 
  EC2 instance и у неё появятся права на что-то. Используется для временных решений или для выдачи прав сервисам на взаимодействие с 
  другими сервисами.
  
Identity Provider - позволяет подключить внешние identity store, например, MS Active Directory. OpenID, SAML 2.0
