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

<p> Quando vocês deseja fazer alterações num código mas não quer que um possível erro causado por elas se espalhe pelo software há um meio de fazer isso. Ao criar um branch você pode como que clonar todo o projeto para uma linha isolada, e assim você aplica as alterações nela, e se tudo ocorrer bem você une ela à linhagem que a deu origem.</p>
<p> Num projeto git por padrão você trabalhará numa branch chamada master. Esta é a branch de produção, ou seja, a branch que contém o software no estado que os usuários veem. Todas as vezes que um software atualiza, essa é a branch de atualização. </p>
<p> Os programadores criam uma branch que se origina na master, chamada develop, e essa é a branch que os desenvolvedores terão acesso. Quando a develop está com mudanças significativas e estáveis, ela é unida à master, para que os usuários tenham acesso à mudança. </p>
<p> Os nomes utilizados nas branches  seguem um padrão, e são eles: </p>
<ul>  
  <li> master (branch de produção) </li>
  <li> develop (branch de desenvolvimento) que se origina na master </li>
  <li> feature (branch de uma nova funcionalidade) que se origina na develop </li>
  <li> bugfix (branch de correção de bugs) que se origina na develop </li>
  <li> hotfix (branch de correção de bugs urgentes) que se origina na master </li>
</ul>
<p> Para verificar em qual branch você está no momento basta usar um: </p>
````
  git branch
````
<p> Caso queira criar uma nova branch, você deve, em primeiro lugar, ir para a branch que deve ser copiada. Por exemplo, sempre que eu quiser criar uma branch de feature nova, antes eu devo me mover para a develop, então poderei criar a branch. Com o comando abaixo você pode criar uma nova branch.</p>
````
  git branch nomeDaBranchQueVoceQuerCriar
````
<p> Com o temmpo será necessário deletar branches. Para isso você deve sair dela e executar o comando abaixo: </p>
````
    git branch -d nomeDaBranchQueVaiSerDeletada
````
<p> Caso você queira deletar mais de uma ao mesmo tempo, poderá colocar vários nomes de branches após o -d, todos separados por espaço. Nunca delete a master ou a develop, elas  existirão durante todo o projeot de forma permanente. </p>

<h3> git checkout </h3>
<p> Para trocar a branch em que você está você pode usar um: </p>
````
  git  checkout nomeDaBranchQueVoceQuerIr
````
<p> Caso você queira criar uma nova branch e ir imediatamente para ela o comando abaixo faz isso: </p>
````
  git checkout -b nomeDaBranchQueVaiSerCriada
````
<p> Se você não quiser usar o comando acima, poderá fazer da forma mais longa, usando o git branch e depois o git checkout. </p>
