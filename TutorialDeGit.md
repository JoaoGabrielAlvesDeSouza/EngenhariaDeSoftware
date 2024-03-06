<h1> Tutorial de Git </h1>

<h2> Neste arquivo teremos uma série de exemplos de execução de comandos básicos do git, bem como a recomendação de vídeos demonstrando de forma prática o que eles fazem. </h2>

<h3> Introdução ao o que é o git </h3>
<p> <a href = "https://www.youtube.com/watch?v=beMnH51P-T4&list=PLmMxPWmzYRGcTabffOwHBORBjtKa2wCXS"> O que é uma ferramenta de controle de versão? </a> </p>
<p> <a href = "https://www.youtube.com/watch?v=s_Jp_ohfBQw&list=PLmMxPWmzYRGcTabffOwHBORBjtKa2wCXS&index=2"> O que é e como funciona o git. </a> </p>

<h3> Configurações iniciais do git </h3>

<p> Ao instalar o git no seu computador, abra o git bach e execute os seguintes comandos, um por vez: </p>

````
  git config --global user.name = "Seu Nome"
  git config --global user.email = "Seu Email"
````

<p> Com isso toodas as vezes que você for trabalhar num projeto compartilhado será possível identificar que você fe algo, seja para te perguntar como aquele trecho de código funciona ou para te reportar um bug no que você fez. </p>

<h3> Comandos básicos do git </h3>

<h5> git add </h5>

<p> Se você viu os vídeos acima sabe como e git funciona. Usando o git add você move os arquivos para a área de preparo, onde os arquivos serão preparados para serem salvos. Com o comando abaixo você pode fazer isso: </p>

````
  git add .
````

<h3> git commit </h3>
<p> Ao criar um commit você salva aquela versão do arquivo. Isso faz com que haja um ponto de restauração ali que poderá ser usado para retornar àquele ponto do código. </p>

````
  git commit -m "fix: erro de requisição consertado"
````
<p> Acima temos um exemplo de commit. A tag -m é passada para que não seja necessário editar o texto no bloco de notas ou editor que você tiver. O préfixo fix indica que o commit se trata de uma correção no código. Há uma padronização de como devem ser feitos os commits. </p>
<p> os mais usados são: </p>
<ul>  
  <li> fix para correções </li>
  <li> feat para novas funcionalidades </li>
  <li> docs para documentação </li>
</ul>

<h3> git branch </h3>
<p> O git branch cria uma nova ramificação do git, isso faz com que você possa criar a sua e modificar ela, e se suas modificações funcionarem você une ela com a branch de onde ela veio, e caso suas modificações deem errado você pode apagar a branch que você criou. </p>
<p> É quase como se você copiasse o projeto todo, modificasse ele e se funcionar você une ele ao antigo. Assim ao invés de alterar o projeto  diretamente você altera apenas a branch. O comando abaixo apenas permite com que você visualize a branch em que você está (por  padrão é a master). </p>

````
  git branch
````

<h3> git checkout </h3>
<p> O git checkout te permite trocar de branches. </p>

````
git checkout nomeDaBranchDeDestino
````

<p> Outra utilizade dele é criar uma branch e te mover para ela. </p>

````
  git git checkout -b nomeDaBranch
````

<h3> git merge </h3>

<p> Depois de criar uma branch e realizar as alterações desejadas você deve uní-la à branch de onde ela se originou. </p>

````
git checkout branchDeOrigem
git merge branchOndeForamFeitasAsAlteracoes
````

<p> Após isso a branchOndeForamFeitasAsAlteracoes será unida a branchDeOrigem. Você deverá deletar a branchOndeForamFeitasAsAlteracoes. </p>

````
git branch -d branchOndeForamFeitasAsAlteracoes
````
