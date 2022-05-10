# Git-Github
### Uma revisão bem detalhada sobre todas as funcionalidades do Git e Github que conheço

![Simbolo Git e GitHub](https://github.com/DanielKlimach/Git-Github/blob/master/Github.png)

<ul>
<li>git config --global user.name "nome que quiser" (configura o nome do usuario do git)</li>
<li>git config --global user.email "email que quiser" (configura o email do usuario do git)</li>
<li>git config user.email (mostra o email que está sendo utilizado)</li>
<li>git config user.name (mostra o nome que está sendo utilizado)</li>
</ul>

<ul>
<li>git config core.editor (mostra o caminho que o git está vinculado, em algum programa, caso não tenha digite:<br/>
git config core. editor "diretório do programa desejado" [vincula um programa com o git, no meu caso é o Visual Studio Code]<br/>
Além disso você precisa:<br>
Clicar com o botão direito no programa que você vinculou no git [ex:Visual Studio Code], depois
ir em propriedades, em Destino, copie seu diretório, depois vá no painel de controle > sistema e seguraça > sistema >
configurações avançadas do sistema > variáveis de ambiente > novo... > nome da variável: nome que quiser [ex:code]
valor da variável: cole o diretório copiado > dê ok em tudo
</ul>

<ul>
<li>Agora se escrever o nome da variável que colocou [ex: code] o git abrirá automaticamente o programa vinculado[ex: Visual Studio Code]</li>
</ul>

<ul>
<li>pwd (mostra o diretório que aquele documento git está vinculado)</li>
<li>ls (mostra uma lista de todos os aqueivos e pastas daquele diretório)</li>
<li>clear (limpa a tela)</li>
<li>cd (entra dentro de uma pasta, usado para entrar em um diretório desejado)<br>
[ex: cd \c > cd \Users > cd \DELL > cd \OneDrive > cd \Documentos > cd \Estudos]</li>
</ul>

<ul>
<li>mkdir "nome que quiser" (cria uma pasta no diretório selecionado com o cd)</li>
<li>touch "nome que quiser.tipo_do_arquivo"[ex: exemplo.txt] (cria um arquivo com o nome que colocar
e do tipo que colocar depois do ".")</li>
</ul>

<ul>
<li>Ou vá em uma pasta que queira vincular seus projetos com o git e clique com o botão direito e logo clique em git bash here<br>
(ele ja seleciona aquele diretório para fazer alterações sem precisar usar os comandos cd, ls, touch e etc)</li>
</ul>

<ul>
<li>git init (cria uma pasta git para trabalhar com os arquivos que tem ali, e execultar muitos outros comandos)<br>
{não esqueça de selecionar o diretório com o git dash here ou manualmente}</li>
<li>Para ver a pasta .git você precisa ir no menu da pasta selecionada clicar em exibir > Mostrar/Ocultar > Selecionar Itens Ocultos</li>
<li>Dentro dessa pasta que todo o seu conteúdo será armazenado pelo git</li>
<li>Na pasta Objects dentro do .git que ficará os commits que verá mais pra frente</li>
</ul>

<ul>
<li>git status (diz se tem algum arquivo que precisa ser adicionado a pasta .git{repositório} ou não)</li>
<li>quando estiver em vermelho é porque não foi adicionado ao repositório, quando estiver verde é porque foi,<br>
mas quando está todas as etapas concluidas (adicionado ao repositório e criado um commit) aparece nothing to commit, working tree clean</li>
<li>git add "nome do arquivo.tipo do arquivo" (para adicionar um arquivo específico ao repositório)</li>
<li>git add . ou git add * (adiciona todos os arquivos daquela pasta ao repositório)</li>
</ul>

<ul>
<li>git commit -m "nome que quiser" (cria uma versão de armazenamento dos arquivos)</li>
<li>git log (mostra as versões{commits} criados naquele .git e por quem com nome e email)</li>
<li>git log --oneline (mostra as versões{commits} do git com seu nome e seu código de versão,  uma maneira melhor)</li>
<li>git add . (armazena os arquivos em um container) git commit -m "nome" (adiciona o container ao repositório .git)</li>
</ul>

<ul>
<li>master é o ramo de commits principal, head é o commit que está selecionado</li>
<li>git commit -am "comentário do commit" (eu ja adiciono o arquivo ao container <br/> e já crio uma commit para aquele container, tudo em uma linha só)</li>
</ul>

<ul>
<li>git log --graph (cria um gráfico dos seus commits, facilita se localizar)</li>
<li>git commit --amend -m "nova mensagem" (para renomear o ultimo commit selecionado) NESSEITA DE REVISÃO</li>
<li>além das versões{commits} criados, você pode criar ramos de commits para trabalhar separadamente<br/>
(master é o ramo principal, esses ramos são chamados de branchs ou no singular branch)</li>
<li>git branch (mostras as branchs {ramos} que você possui)</li>
<li>hash é o id de cada commit, cada commit tem seu id{hash}</li>
<li>git checkout "hash" (para mudar de commits{versões})<br>
(para ver o hash de cada commit basta escrever git log --oneline)</li>
-quando você usar o checkout as versões posteriores a ela, ficarão anexadas na branch master,<br/>
já a versão selecionada e as versões anteriores serão desanexadas da branch master,<br/>
caso queira retornar as versões posteriores você precisará escrever: git checkout "master"<br/>
(no caso a branch master que sofrerá essas alterações porque é com ela que estamos trabalhando)

-git diff (mostra as alterações que você fez em seus arquivos, verde é o que escreveu, vermelho é oque apagou)<br/>
-git reset HEAD (caso você tenha atualizado ou adicionado um arquivo e colocado ele no container com o git add,<br/>
mas ainda não adicionou o container ao seu commit com git commit "nome", e se arrependeu de suas alterações você pode<br/>
digitar esse comando para desfazer as alteraçõeam s, mas depois terá que usar o git add mais uma vez)

-git reset --hard "hash" (para apagar seus commits e voltar até o hash selecionado,<br/>
enquanto não chegar no commit desejado ele irá apagar os demais)

-git checkout -b "Nome" (Cria uma nova ramificação{branch}, já com todos os commits do ramo que estava sendo utilizado)<br/>
-git merge "nome" para fundir as branchs, primeiro vc tem que estar na branch master, depois escrever<br/>
o código com o nome da branch que você quer fundir)<br/>
-Se o código for o mesmo um deles continua, não duplica, se um linha estiver diferente da outra aparecerá conflit no git,<br/>
para resolver você entra no programa que está usando e aparecerá a opção de manter uma linha e excluir a outra, vice-versa,<br/>
maanter as duas linhas ou fazer uma comparação automática <br/>
-depois de resolver os conflitos você tem que fazer um novo add e commit, então ele fará o merge automaticamente no novo commit<br/>
-git merge --abort (abortar o marge quando houver um conflito)


-git remote -(verifica se tem algum repositório remoto, além do local que ele está vinculado)<br/>
Se não tiver, não aparecerá nada 

-quando você cria um repositório no github aparecerá instruções<br/>
do que fazer para vincular o git com ele, antes clique na opção https

-git remote add origin "link do repositório" (vincular o projeto git a um repositório remoto)

-git push -u origin "master" (coloca o conteúdo da branch master no link remoto)<br/>
-a primeira vez que você fizer isso o git vai pedir para você se autenticar<br/>
-depois de fazer esse processo as próximas pode apenas digitar git push que ele atualizará no link remoto

-erro:403 permission denied (erro de autenticação - vá em gerenciador de credenciais ><br/>
credenciais do windows > em credenciais genericas terá a credencial do GitHub > clique em remover ><br/>
volte ao git e use o código git push que antes tinha dado erro, vai aparecer a opção de se logar,<br/>
em cime clique na opção token, vá no GitHub > settings > Developer Setings > Personal Accers Tokens ><br/>
> Generate new token > em Note escreva o nome do token que quiser > escolha a data de expiração do token ><br/>
marque todas as caixas em negritos[permita todos os acessos] > Generate Token > Copie o token e salve em algum lugar<br/>
pois ele não será exibido novamente > cole o token no menu de login de token do git > escreva git push e dará certo<br/>
Esse problema vem quando se quer acessas seu código remotamente

-Para clonar um repositório você entra em um repositório do git e clique na opção clone or download ><br/>
copie o link, vá em uma pasta onde você quer que o projeto(repositório fique), clique em git dash here<br/>
depois escreva: git clone "link copiado"

-Para editar o arquivo direto no github e aplicar as alterações no git local você deve clicar no lápis (edit file)<br/>
editar o que quiser, depois Escreva o nome da commit no commit changes, depois clique no botão commit changes, eu também<br/>
posso criar novos arquivos no meu repositório direto no git, quando for criar um novo arquivo se eu digitar "nomeDaPasta"/nomeDoArquivo<br/>
essa barra fará eu criar uma pasta no meu repositório e dentro dessa pasta terá meu novo arquivo criado, mas também terá que criar um novo<br/>
commit no gitHub que também estará embaixo da sua criação de arquivos,<br/>
-git pull (para vincular as alterações do GitHub para o Git) 

-Depois de digitar o Git Log você terá que apertar a tecla Q para ele voltar a opção de digitar códigos

-Outra situação possível de conflito é entre duas commits em um repositório remoto (Ex: trabalho em um projeto em um pc doméstico e em outro pc da faculdade, onde<br/>
faço o git push das minhas comits para o github como repositório remoto, um dia fiz alterações no meu projeto do pc da faculdade e dei git push, 
outro dia fui mexer no meu<br/>
pc doméstico, mas as alterações do meu projeto que fiz na faculdade não estavam salvas naquele pc doméstico, mas mesmo assim resolvi editar os códigos com outras<br/> informações, então quando fui dar git push da minha nova commit deu conflito de commits no meu repositório remoto, o github)

-git fetch (faz o download ds alterações no meu repositório remoto, para eu editar e resolver o conflito explicado acima,<br/>
ele equivale ao git pull mas o fetch além disso faz o merge entre as commits)

-depois do comando fetch digite o comando: git remote (para ver o seu repositório remoto [ex:origin],
depois de um: git checkout "nome do repositório" (ex:origin), para visualisar o git e os arquivos para a atualização daquele repositório, depois mude de volta para o repositório principal: git checkout "master", depois eu digito git pull e ele me mostrará os conflitos que estão tendo entre os commits, depois de resolver os conflitos, eu digito git add . (para adicionar as alteraçõs),
depois git commit "nome que quiser" (para criar um novo commit com os conflitos resolvidos) e então git push

-independente do tipo de arquivo que vc esteja trabalhando no seu projeto, vc pode fazer as alterações em qualquer programa que quiser, por exemplo, estou trabalhando
nesse projeto com o notepad++, mas o Visual Studio é muito bom para resolver conflitos, pois aparece  os menus do que você vai querer fazer, então na hora de resolver
conflitos eu posso resolver no Visual, mas depois continuar trabalhando no notepad++ sem problemas, inclusive o Visual é meu editor padrão do git, que eu configurei
 
-você pode entrar nos repositórios dos outros no github e clicar em fork, no canto superio direito, quando você for nos seus repositórios estará o clone do projeto que você deu fork
(ele exibe de onde veio o projeto, posso fazer o que quiser, novas commits etc que não irá interferir no projeto autentico do dono do repositório)
-quando você altera, em cima do código que você alterou, mostra quantos contribuidores daquele código tem
-caso eu queira sugerir a alteração que fiz para o dono do repositório eu clico em new pull request, na página principal do repositório específico,
ele mostra as suas alterações, então você clica em new pull-request, então aparecerá um comentário para você descrever sua alteração para o dono

-Caso você receba new pull request do seu código aparecerá um novo número de pull request no seu repositório, você clica na aba pull request, então aparecerá
o comentário da pessoa que te enviou com o link do commit que ele fez, então clica nele e mostrará as alterações daquele commit em relação ao seu commit principal
eu clico em conversation para voltar ao comentário do pull request e se você gostar das alterações clique em merge pull request > confirm merge, no seu repositório
mostrará que você aceitou um pull request no seu projeto.

-git push -f origin master (você irá substituir o conteúdo da branch remota pelo código que você tem no seu repositório local)

### Referências
[Primeiro Vídeo da Playlist de referência](https://www.youtube.com/watch?v=FF1f4bKYhoo&list=PLbEOwbQR9lqzK14I7OOeREEIE4k6rjgIj&index=2 "Vídeo de Introdução ao Curso")
