# Github ---> Gitlab repository mirroring

1. Gitlab'da sync edilecek project oluşturulur. (Örnek proje adı: smm)
2. Gitlab'da yeni bir kullanıcı oluşturulur. (Örnek kullanıcı adı: smmuser)
3. Oluşturulan kullanıcı yeni project altında maintainer olarak yetkilendirilir (Projects -->> smm -->> Manage access -->> Invite Members, eklenditen sonra role maintainer olarak belirlenir)
4. Mirrorring için project ayarlarından access token oluşturulur. Bu acces token maintainer rolüne sahip olmalıdır (Projects -->> Settings -->> Access Tokens, Örneğin "GITLAB_TOKEN")
5. Gitlab tarafında oluşturulan access token Github tarafında mirror yapılacak repository ayarlarına repository secret olarak girilir (Repository -->> Settings -->> Sercrets and variables -->> Actions -->> Repository secrets, Örneğin "GITLAB_TOKEN")
6. Github tarafında repository içerisine ".github/workflows/mirror-to-gitlab.yml" dosyası ile pipeline oluşturulur.

Böylelikle mirror pipeline'ı hazırlanmış olur.


