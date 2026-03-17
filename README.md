# URL do site criado:
https://minemaker.github.io/site-proficiencia/

--------

# Como executar, caso não queira acessar URL:
Clonar repositório
1. git clone https://github.com/SEU-USUARIO/NOME-DO-REPO.git<br>
Entrar no diretório
2. cd NOME-DO-REPO<br>
Abrir no navegador
3. xdg-open index.html

--------

Comandos usados para realizar a tarefa:

1. sudo apt install git
2. sudo apt install gh

3. mkdir otavio-site
4. cd otavio-site
5. git init
6. nano index.html       //Aqui eu fiz o arquivo html
7. git add .
8. git commit -m "Subindo o site pro git, primeira versão"
9. gh auth login         //Comando para logar na conta do github, seguindo passo a passo que aparece no terminal
10. git branch -M main
11. gh repo create site-proficiencia --public --source=. --remote=origin --push
12. gh api -X POST repos/MINEMAKER/site-proficiencia/pages \
-H "Accept: application/vnd.github+json" \
--input - <<EOF
{
  "source": {
    "branch": "main",
    "path": "/"
  }
}
EOF
