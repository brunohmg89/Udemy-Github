# Github - Udemy

## Seção 1: Introdução e instalação das dependências

1. Introdução

    Introdução ao que aprenderemos durante o curso, comandos e conceitos sobre Git e GitHub.

2. Apresentação do curso

    Apresentação de como foi separadas as seções e de que forma iremos aprender.

3.  Instalando o Git no Windows
    Instalando git via chocolatey: `choco install git` ou instalando baixando o executável nesse link <https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git>

4. Instalando o Git no Linux
    Só utilizar o melhor gerenciador de pacotes, como o YUM `sudo yum install git-all` ou APT `sudo apt-get install git-all` seguindo esse link: <https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git>

5. Instalando o VS Code no Windowns
    Instalando o VS Code, baixar o executável nesse link <https://code.visualstudio.com/download>

6. Instalando o VS Code no Linux
    Instalando o VS Code, baixar o melhor executável nesse link <https://code.visualstudio.com/download>

7. O que é controle de versão
    - Uma técnica que ajuda a gerenciar o código-fonte de uma aplicação;
    - Registrando todas as modificações de código, podendo também reverter as mesmas;
    - Criar versões de um software em diferentes estágios, podendo alterar facilmente entre elas;
    - Cada membro da equipe pode trabalhar em uma versão diferente;
    - Há ferramentas para trabalhar o controle de versão com GIT e SVN.

8. O que é Git
    - O sistema de controle de versão mais utilizado no mundo atualmente;
    - O Git é baseado em repositórios, que contêm todas as versões do código e também  as cópias de cada desenvolvedor;
    - Todas as operações do Git são otimizadas para ter alto desempenho;
    - Todos os objetos do Git são protegidos com criptografia para evitar alterações indevidas e maliciosas;
    - O Git é um projeto de código aberto

9. Como tirar o máximo de proveito do curso
    - Codificar junto
    - Criar exemplos
    - Criar outros casos usando os exemplos passados
    - Ouvir e depois praticar

10. Slides do curso
    - Arquivo PDF com os slides do curso.

11. Link do repositório do portfólio
    - <https://github.com/matheusbattisti/matheusbattisti.github.io>

12. Indicações de livros
    - Livro: <https://amzn.to/3ULsWwH>

13. Conclusão da primeira seção
    - Conclusão da introdução e da instalação das principais dependências.

## Seção 2: Git fundamental

14. Introdução da seção
    - Iremos aprender comandos fundamentais do Git

15. O que é um repositório
    - Onde o código será armazenado;
    - Na maioria das vezes cada projeto tem um repositório;
    - Quando criamos um repositório estamos iniciando um projeto;
    - O repositório pode ir para servidores que são especializados em gerenciar repos, como GitHub e BitBucket;
    - Cada um dos desenvolvedores do time pode baixar o repositório e criar versões diferentes em sua máquina.

16. Criando um repositório
    - Para criar um repositório utilizamos o comando `git init`
    - Desta maneira o git vai criar os arquivos necessários para inicializa-lo;
    - Que estão na pasta oculta `.git`
    - Após este comando o diretório atual será reconhecido pelo git como um projeto e responderá aos seus demais comandos.
    - Comandos:
        - `git status` para verificar se existe um repositório ativo
        - `git init` para iniciar um projeto de um diretório.

17. O que é GitHub
    - É um serviço para gerenciar repositórios, gratuito e amplamente utilizado;
    - Podemos enviar nossos projetos para o GitHub e disponibiliza-lo para outros devs;
    - O GitHub é gratuito tanto para projetos públicos como privados;
    - Criando uma conta no <https://github.com/>

18. Mudança do nome principal de branch
    - Alteração de alguns anos atrás da branch principal de `master` para `main`

19. Enviando repositórios para o GitHub
    - Podemos facilmente enviar nossos repos para o GitHub;
    - Precisamos criar o projeto no GitHub (entrando no site do GitHub e clicar em `New` e depois das primeiras configurações clicar em `create repository`), inicializar o mesmo no Git em nossa máquina, sincronizar com o GitHub e enviar;
    - Comandos e instruções:
        - Criar um diretório em sua máquina local;
        - Criar um arquivo qualquer dentro do diretório;
        - Inicializar o repositório `git init`
        - Verificar modificações `git status`
        - Adicionar arquivos novos ou alterados `git add NOMEDOARQUIVO` ou `git add .` para adicionar todos os novos arquivos.
        - Realizar o commit dos novos arquivos `git commit -m "MENSAGEM"`, a flag `-m` é de "mensagem" que será apresentado ao enviar as alterações para o repositório, veja mais sobre "conventional commits" nesse link <https://www.conventionalcommits.org/en/v1.0.0/>
        - Criando uma branch principal para o repositório `git branch -M main`
        - Sincronizando origem do repositório com o que foi criado `git remote add origin https://github.com/USUARIOGH/NOMEREPO.git`
        - Enviando as modificações para o repo criado `git push -u origin main` 
        - E esta sequência que parece ser complexa é facilmente executada por poucos comandos;
        - Vale lembrar que só fazemos uma vez por projeto este fluxo;
        - Porém alguns dos comandos utilizados vão ser úteis ao longo do curso;

20. Verificando alterações
    - As mudanças do projeto podem ser verificadas por `git status`
    - Existem arquivos modificados que aparecem como `Modified` e novos arquivo que aparecem como `Untracked`
    - Este comando é utilizado frequentemente;
    - Aqui serão mapeadas todas as alterações do projeto;
    - Como: arquivos não monitorados e arquivos modificados;
    - Podemos também dizer que é a diferença do que já está enviado ao servidor ou salvo no projeto

21. Adicionando arquivos ao projeto
    - Para adicionar arquivos a um projeto utilizamos `git add`
    - Podemos adicionar um arquivo especifico como também diversos de uma só vez;
        - `git add NOMEDOARQUIVO` adicionando um arquivo especifico
        - `git add .` adicionando todos os arquivos modificos de uma vez.
    - Somente adicionando arquivos eles serão "monitorados" pelo git;
    - Ou seja, se não adicionar ele não estará no controle de versão;
    - É interessante utilizar este comando de tempos em tempos para não perder algo por descuido.

22. Salvando alterações
    - As alterações salvas do projeto são realizadas por `git commit`
    - Podemos commitar arquivos especificos ou vários de uma vez com a flag `-a`
        - `git commit NOMEDOARQUIVO -m "MENSAGEM"` "commita" um único arquivo.
        - `git commit -a -m "MENSAGEM"` para "commitar" todos os arquivos, sem a flag `-a` também funciona commitar todos os arquivos.
    - É uma boa prática enviar uma mensagem a cada commit, com as alterações que foram realizadas;
    - A mensagem pode ser adicionada com a flag `-m`

23. Enviando código para o repositório
    - Quando finalizamos uma funcionalidade nova, enviamos o código ao repo remoto, que é o código-fonte;
    - Esta ação é feita pelo `git push` (Estamos trabalhando diretamente na main/master)
    - Após esta ação o código do servidor será utilizado baseando-se no código local enviado

24. Recebendo alterações
    - É comum também ter que sincronizar o local com as mudanças do remoto;
    - Esta ação é feito por `git pull`
    - Após o comando serão buscadas atualizações, se encontradas elas serão unidas ao código atual existente na nossa máquinas.

25. Clonando repositórios
    - O ato de baixar um repositório de um servidor remoto é chamado de clonar repositório;
    - Para esta ação utilizamos `git clone LINKDOREPOSITORIO .` (para pegar o link, só ir no site do GitHub, ir na opção `Code` e copiar o link).
    - Passando a referência do repositório remoto;
    - Este comando é utilizado quando entramos em um novo projeto, por exemplo.

26. Removendo arquivos
    - Os arquivos podem ser deletados da monitoração do Git;
    - O comando para deletar é `git rm`
    - Após deletar um arquivo do Git ele não terá mais suas atualizações consideradas pelo Git;
    - Apenas quando for adicionado novamente pelo `git add`

27. Verificando as alterações por meio de log
    - Podemos acessar um log de modificações feitas no projeto;
    - O comando para este recurso é `git log`
    - Você receberá uma informação dos commits realizados no projeto até então.

28. Renomeando arquivos
    - Com o comando `git mv` podemos renomear um arquivo;
    - O mesmo também pode ser removido para outra pasta;
    - E isso fará com que este novo arquivo seja monitorado pelo Git;
    - O arquivo anterior é excluído.

29. Desfazendo operações
    - O arquivo modificado pode ser retornado ao seu estado original;
    - O comando utilizado é o `git checkout NOMEDOARQUIVO` (volta o estado original do arquivo)
    - Após a utilização do mesmo o arquivo sai do staging;
    - Caso seja feita uma próxima alteração ele entra em staging novamente

30. Ignorando arquivos e diretórios em um projeto
    - Uma técnica muito utilizada é ignorar arquivos do projeto;
    - Devemos inserir um arquivo chamado `.gitignore` na raiz do projeto;
    - Nele podemos inserir todos os arquivos que não devem entrar no versionamento;
    - Isso é útil para arquivos gerados automaticamente ou arquivos que contêm informações sensiveis

31. Resetando um branch
    - Com o comando `git reset` podemos resetar as mudanças feitas
    - Geralmente é utilizado com a flag `--hard`
    - Comando: `git reset --hard origin/NOMEDABRANCH` faz com que reset a branch atual deixando no mesmo estado que está na branch que você aponte.
    - Todas as alterações "commitadas" e também as pendentes serão excluídas

32. Conclusão da seção
    - Concluindo seção com comandos fundamentais do Git.
    - Resumo dos comandos:
        - `git init` *para iniciar o diretório como um repositório*
        - `git status` *para verificar os arquivos criados, não commitados e não trackeados*
        - `git add NOMEDOARQUIVO` *para adicionar um arquivo especifico* ou `git add .` *para adicionar todos os arquivos untracked ou arquivos novos*
        - `git commit NOMEDOARQUIVO -m "MENSAGEM"` *para commitar um arquivo especifico que já está sendo monitorado pelo git ou simplesmente arquivos que foram modificados*
        - `git commit -a -m "MENSAGEM"` *para commitar todos os arquivos adicionados*
        - `git push` *para enviar todos os arquivos commitados para o repositório*
        - `git pull` *para pegar alterações realizadas de forma manual no repositório*
        - `git clone LINKDOREPOSITORIO .` *para clonar um repositório existente*
        - `git rm NOMEDOARQUIVO` *para remover arquivos adicionados*
        - `git log` *para verificar todos os commits realizados e as alterações nela contidas*
        - `git mv` *para mover arquivos de lugar ou renomear os arquivos*
        - `git checkout NOMEDOARQUIVO` *para voltar o arquivo alterado para seu estado original antes da alteração*
        - Arquivo `.gitignore` *utilizado para ignorar arquivos dentro do diretório e não envia-los para o repositório*
        - `git reset --hard origin/NOMEDABRANCH` *utilizado para resetar a branch toda e todas as alterações que foram feitas até então*

    - Teste 1: Quiz sobre os comandos fundamentais
        - Contém 4 perguntas, 100% de acerto

## Seção 3: Trabalhando com Branches

33. Introdução sobre a seção
    - Introdução breve do que aprenderemos na seção "trabalhando com branches"

34. O que são Branches
    - Branch é uma forma que o Git separa as versões dos projetos;
    - Quando um projeto é criado ele inicia na branch `main`, estamos trabalhando nela até este ponto do curso;
    - Geralmente cada nova feature de um projeto fica em uma branch separada;
    - Após a finalização das alterações os branches são unidos para ter o código-fonte final

35. Criando e visualizando branches
    - Para visualizar os branches disponíveis basta digitar `git branch`
    - Para cria um branch você precisa utilizar o comando `git branch NOMEPARABRANCH`
    - Estas duas operações são muito utilizadas no dia a dia de um dev

36. Deletando branches
    - Podemos deletar um branch com a flg `-d` ou `--delete`
    - Comando: `git branch -d NOMEDABRANCH`
    - Não é comum deletar um branch, normalmente guardamos o histórico do trabalho;
    - Geralmente se usa o delete quando o branch foi criado errado

37. Mudando de branch
    - Podemos mudar para outro branch utilizando o comando `git checkout -b NOMEDABRANCH` (esse comando muda de branch já criando um novo)
    - Esta comando também é utilizado para dispensar mudanças de um arquivo
    - Alterando o branch podemos levar alterações que não foram commitadas junto, tome cuidado

38. Unindo branches
    - O código de dois branches distintos pode ser unido pelo comando `git merge NOMEDABRANCH`
    - Outro comando para a lista dos mais utilizados
    - Normalmente é por meio dele que recebemos as atualizações de outros devs

39. Utilizando a stach
    - Podemos salvar as modificações atuais para prosseguir com uma outra abordagem de solução e não perder o código
    - O comando para esta ação é o `git stash`
    - Após o comando o branch será resetado para a sua versão de acordo com o repo

40. Recuperando stach
    - Podemos verificar as stashs criadas pelo comando `git stash list`
    - E também podemos recuperar a stash com o comando `git stash NOMEDASTASH`
    - Verificando alterações da stash `git stash shown -p NUMERODASTASH`
    - Desta maneira podemos continuar de onde paramos com os arquivos adicionados a stash

41. Removendo a stash
    - Para limpar totalmente as stashs de um branch podemos utilizar o comando `git stash clear`
    - Caso seja necessário deletar uma stash especifica podemos utilizar `git stash drop NUMERODASTASH`

42. Criando Tags
    - Podemos criar tags nos branches por meio do comando `git tag -a NOMEDATAG -m "MENSAGEM"`
    - A tag é diferente do stash, serve como um checkpoint de um branch
    - É utilizada para demonstrar estágios do desenvolvimento de algum recurso

43. Alterando a tag
    - Podemos verificar uma tag com o comando `git show NOMEDATAG`
    - Podemos trocar de tags com o comando `git checkout NOMEDATAG`
    - Desta maneira podemos retroceder ou avançar em checkpoints de um branch

44. Enviando tags ao repositório
    - As tags podem ser enviadas para o repositório de código, senda compartilhada entre os devs
    - O comando é `git push origin NOMEDATAG`
    - Ou se você quiser enviar mais tags `git push origin --tags`

45. Conclusão da seção
    - Concluindo seção com comandos relacionados a branches.
    - Resumo dos comandos:
        - `git branch` *para listar as branches existentes* 
        - `git branch NOMEDABRANCH` *para criar uma branch*
        - `git branch -d NOMEDABRANCH` ou `git branch --delete NOMEDABRANCH`*para deletar uma branch*
        - `git checkout -b NOMEDABRANCH` *para criar uma nova branch saindo da anterior*
        - `git merge NOMEDABRANCH` *para mergear as alterações realizadas em uma branch para outra*
        - `git stash` *para criar um stash*
        - `git stash list` *listar stashs*
        - `git stash NOMEDASTASH` *recuperar uma stash*
        - `git stash shown -p NUMERODASTASH` *listar as alterações da stash*
        - `git stash clear` *limpar todas as stashs*
        - `git stash drop NUMERODASTASH` *limpar stash especifica*
        - `git tag -a NOMEDATAG -m "MENSAGEM"` *criando uma tag em uma branch*
        - `git tag` *listar tags*
        - `git show NOMEDATAG` *listar alterações contidas na tag*
        - `git checkout NOMEDATAG` *entrar em uma tag*
        - `git push origin NOMEDATAG` *enviar a tag para o repositório*
        - `git push origin --tags` *enviar todas as tags criadas para o repositório*

## Seção 4: Compartilhamento e atualização de repositórios

46. Introdução da seção
    - Introdução breve do que aprenderemos na seção "Compartilhamento e atualização de repositórios"

47. Encontrando branches
    - Branches novos são criados a todo tempo e o seu git pode não estar mapeando eles
    - Com o comando `git fetch` você é atualizado de todos os branches e tags que ainda não estão reconhecidos por você
    - Este comando é útil para utilizar o branch de algum outro dev do time, por exemplo

48. Recebendo atualizações
    - O comando `git pull` serve para recebermos atualizações do repositório remoto
    - Cada branch pode ser atualizada com o git pull
    - Utilizamos para atualizar a main do repo como também quando trabalhamos em conjunto e queremos receber atualizações de uma dev

49. Enviando alterações
    - O comando `git push` faz o inverso do pull, ele envia as alterações para o repo remoto
    - Serve também para enviar as atualizações de um branch especifico para um outro dev
    - Ou quando terminamos uma tarefa e precisamos enviar ao repo

50. Utilizando o remote
    - Com o `git remote` podemos fazer algumas ações como, adicionar um repo para trackear ou remover
    - Quando criamos um repo remoto, adicionamos ele ao git com o comando `git remote add origin LINKDOREPO`

51. Conhecendo os submodules
    - Submódulo é a maneira que temos de possuir dois ou mais projetos em um só repositório
    - Podemos adicionar uma dependência ao nosso projeto atual, porém mantendo suas estruturas separadas
    - Para adicionar o submódulo utilizamos o comando `git submodule add REPO`
    - Para verificar os submódulos o comando é `git submodule`

52. Atualizando os Submódulos
    - Para atualizar um submódulo primeiro devemos commitar as mudanças
    - E para enviar para o repositório do submódulo utilizamos `git push --recurse-submodules=on-demand`
    - Este fluxo fará a atualização apenas do submódulo

53. Conclusão da seção
    - Concluindo seção com compartilhamento e atualização de repositórios.
    - Resumo dos comandos:
        - `git fetch` *para "baixar" as branchs e tags do repositório remoto*
        - `git pull` *serve para baixar as atualizações da branch*
        - `git push` *serve para enviar todas as alterações realizadas para a branch remota*
        - `git remote` *atrela ou sincroniza um repositório a um diretório*
        - `git remote -v` *mostra a origem do repositório*
        - `git remote rm origin` *remove ou desacocla o diretório do repositório remoto*
        - `git remote add origin LINKDOREPOSITORIO` *sincroniza um repositório novamente ao diretório local*
        - `git submodule` *mostra os submodelos de um repositório*
        - `git submodule add REPO` *adiciona um repositório dentro de outro*
        - `git push --recurse-submodules=on-demand` *esse push faz com que a atualização seja realizado no repositório de origem*

## Seção 5: Análise e inspeção de repositórios

54. Introdução da seção
    - Introdução breve do que aprenderemos na seção "análise e inspeção de repositório"

55. Exibindo detalhes de branches e tags
    - O comando `git show` nos dá diversas informações úteis
    - Ele nos dá as informações do branch atual e também seus commits
    - As modificações de arquivos entre cada commit também são exibidas
    - Podemos exibir as informações de tags também com o comando `git show TAG`

56. Verificando diferenças
    - O comando `git diff` serve para exibir as diferenças de uma branch
    - Quando utilizado as diferenças do branch atual com o remoto serão exibidas no terminal
    - Podemos também verificar a diferença entre arquivos `git diff ARQUIVO1 ARQUIVO2`

57. Log de atividades resumido
    - O comando `git shortlog` nos dá um log resumido do projeto
    - Cada commit será unido por nome do autor
    - Podemos então saber quais commits foram enviados ao projeto e por quem

58. Conclusão da seção
    - Concluindo seção de análise e inspeção de repositórios
    - Resumo dos comandos:
        - `git show` *mostra informações sobre todas as alterações realizados no repositório*
        - `git show TAG` *mostra as informações sobre todas as alterações realizados em Tags no repositório*
        - `git diff` *mostra todas as alterações nos arquivos que foram realizadas*
        - `git diff HEAD:ARQUIVO1 ARQUIVO1` *mostra as diferenças entre o arquivo local e do repositório*
        - `git shortlog` *nos dá um log resumidos de todos os commits que foram realizados no repositório*

## Seção 6: Administração de repositórios

59. Introdução da seção
    - Introdução breve do que aprenderemos na seção de "administração de repositórios"

60. Limpando arquivos untracked
    - O comando `git clean -f` vai verificar e limpar arquivos que não estão sendo trackeados
    - Ou seja, todos os arquivos que você não utilizou o `git add`
    - Utilizado para arquivos que são gerados automaticamente, por exemplo, e atrapalham a visualização do que é realmente importante

61. Otimizando repositórios
    - O comando `git gc` é uma abreviação para "garbage collector"
    - Ele indica arquivos que não são mais necessários e os exclui
    - Isso fará com o que o repositório seja otimizado em questões de performance

62. Verificando integridade dos arquivos
    - O comando `git fsck` é uma abreviação de "File System ChecK"
    - Esta instrução verifica a integridade de arquivos e sua conectividade
    - Verificando assim possíveis corrupções em arquivos
    - Comando de rotina, utilizado para ver se está tudo certo com nossos arquivos

63. Reflog
    - O `git reflog` vai mapear todos os seus passos no repositório, até uma mudança de branch é inserida neste log
    - Já o `git log`, que vimos anteriormente, apenas armazena os commits de uma branch
    - Os reflogs ficam salvos até expirar, o tempo de expiração padrão é de 30 dias

64. Comprimindo o repositório
    - Com o comando `git archive` podemos transformar o repositório em um arquivo compactado, por exemplo
    - O comando é `git archive --format zip --output main_files.zip main`
    - E então a master vai estar zipada no arquivo "master_files.zip"

65. Conclusão da seção
    - Concluindo seção de administração de repositórios
    - Resumo dos comandos:
        - `git clean -f` *para limpar todos os arquivos que não foram trackeados, ou seja, novos arquivos*
        - `git gc` *limpa arquivos desnecessários para o repositório e os limpa*
        - `git fsck` *faz uma varredura se existe arquivos corrompidos, mantendo a saúde do repositório*
        - `git reflog` *traça todo seu histório de alterações e movimentações no repositório*
        - `git archive --format zip --output NOMEDOARQUIVO.zip main` *cria um arquivo "zipado" de todos o projetos e seus arquivos*

## Seção 7: Melhorando os commits do projetos

66. A importância dos commits
    - O problema: commits sem sentido atrapalham o projeto
    - Precisamos padronizar os commits, para que o projeto cresça de forma saudável também no versionamento, isso ajuda em:
    - Review do Pull Request
    - Melhoria dos logs em `git log`
    - Manutenção do projeto (voltar código, por exemplo)

67. Técnica de private branch
    - Há uma solução chamada private branches
    - Onde criamos branches que não serão compartilhadas no repositório, então podemos colocar qualquer commit
    - Ao fim da solução do problema podemos fazer um rebase
    - O comando será `git rebase BRANCHATUAL BRANCHFUNCIONALIDADE -i`
    - Escolhemos os branches para excluir (squash) e renomear com (reword)

68. Melhorando as mensagens dos commits
    - Separar assunto do corpo da mensagem
    - Assunto com no máximo 50 caracteres
    - Assunto com letra inicial maiúscula
    - Corpo com no máximo 72 caracteres
    - Explicar o porque e como do commit, e não como o código foi escrito
    - Comandos:
        - `git rebase BRANCHATUAL PRIVATEBRANCH -i` *realizado para "mergear" commits com nomenclaturas erradas ou fora do padrão e também para renomear commits ajudando em possíveis tshoots com o `git log`. O conceito de private branch é a criação de uma branch derivadas de outro branch que não seja a main/master*
        - *com o comando abaixo é exemplificado a inserção de um assunto padronizado ao commit e após um "enter" podemos inserir uma explicação mais detalhada do commit*
            ~~~
            git commit -a -m "Assunto do commit
            >> 
            >> inserindo mais uma linha de um commit, exemplificando o corpo da mensagem"
            ~~~
        

## Seção 8: Explorando e entendendo o GitHub

69. Introdução da seção
    - Introdução breve do que aprenderemos na seção "Explorando e entendendo o GitHub"

70. Criando repositório
    - No GitHub inicializamos os repositórios, e temos algumas informações importantes para preencher, vamos vê-las em detalhes:
    - Algumas delas são: Nome do repositório, descrição, licença
    - Tudo poderá ser alterado ao longo do seu projeto, mas é interessante conhecer os detalhes das informações para configurar um projeto.

71. Verificando código fonte e licenças
    - Na aba "Code" teremos acesso a informações importantes, como o próprio código-fonte
    - Podemos checar também uma documentação do projeto pelo `README.md`
    - E os detalhes da licença do projeto
    - Criar branches, adicionar arquivos e muito mais

72. Criando e verificando issues
    - Na aba "Issue" podemos criar tarefas ou possíveis bugs do projeto
    - Interessante para a organização se manter ciente do que ainda precisa fazer ou corrigir
    - Normalmente há um padrão para a criação de novos issues
    - Podemos utilizar o Markdown no texto também (igual no README.md)
    - A issue deve ter uma label e também um responsável

73. Atualizando projeto por Pull Request
    - Na aba "Pull Request" é onde os colaboradores do projeto enviam código para resolver as issues ou adicionar novas funcionalidades ao projeto
    - A ideia é que o código não seja inserido direto na main e sim passe por um Pull Request, para ser analisado
    - O Pull Request vem de um novo branch criado no projeto e enviado para o repositório, com o incremento do código

74. Processos de CI/CD no GitHub
    - Na aba "Actions" é onde se cria as automatizações de deploy com integração em outros serviços
    - Incluindo CI/CD (Continuous Integration / Continuous Development)
    - Ou seja, podemos criar uma rotina de atualizar a main automaticamente e outros processos

75. Criando projetos no GitHub
    - Na aba "Projects" podemos criar um projeto e utilizar um quadro de tarefas
    - Este processo é conhecido como "Kanban" e pode ajudar a organizar seu time, criando notas que podem virar Issues
    - Estrutura interessante: Backlog, Retorno de qualidade, Desenvolvimento, Teste, Finalizada
    - A tela lembro muito o software "Trello"

76. Criando uma "Wiki" no GitHub
    - Na aba "Wiki" podemos criar uma documentação mais extensa para o projeto
    - Como descrever funcionalidades, bugs conhecidos e não solucionados, entre outras funções
    - A ideia é que seja um repositório de conhecimento sobre o projeto

77. Visualizando os dados do projeto
    - Na aba "Insights" temos informações detalhadas do projeto, como:
    - Quem são os contribuidores, commits, forks e muito mais
    - Interessante para entender como o projeto está andando e a sua evolução desde o ínicio

78. Configurações do repositório
    - Na aba "Settings" temos acesso a diversas configurações do projeto
    - É onde podemos alterar o nome do repositório ou remover/adicionar features
    - E também é nela que adicionamos colaboradores ao projeto
    - O repositório pode ser removido nesta aba

79. Criando gists
    - Gist são pequenos blocos de código que podem ser hospedados no GitHub também
    - Você pode armazenar uma solução que achou interessante para algum problema e não quer perder, por exemplo
    - E o link do Gist pode ser compartilhado
    - No fim das contas o Gist acaba sendo um repositório também

80. Buscando repositórios interessantes
    - O GitHub não serve só para salvar os nossos projetos, podemos encontrar repositório interessantes
    - Podemos até aprender com isso também, olhando o código fonte de desenvolvedores experientes
    - E não para por ai, você pode dar "star" nos projetos que gostou ou "fork" nos que deseja continuar em um repo próprio

81. Conclusão da seção
    - Concluindo seção de Explorando e entendendo o GitHub.
    - Resumo:
        - Aba _Code_ onde fica o código do projeto, como README.md
        - Aba _Issue_ onde podemos criar tarefas e bugs para possível resolução
        - Aba _Pull Request_ onde inserimos códigos a partir de uma branch para que outros devs possam analisar antes de ser mergeada com a main
        - Aba _Actions_ onde podemos criar ações para conexões com APIs ou CI/CD
        - Aba _Projects_ onde podemos criar um Kanban, com tarefas e seus estágios de desenvolvimento
        - Aba _Wiki_ onde podemos criar um "repositório de conhecimento" adicionandos tutoriais e passo a passo de alguma solução
        - Aba _Insights_ onde vemos as métricas do repositório
        - Aba _Settings_ onde podemos alterar as configurações do projeto
        - _Gist_ é possível criar um "mini" repositório, criando pequenos arquivos e sendo possível compartilha-los
        - No GitHub existem milhares de repositórios e algum deles pode ser útil para o seu desenvolvimento

## Seção 9: Markdown do básico ao avançado

82. Introdução da seção
    - Introdução breve do que aprenderemos na seção "Markdown do básico ao avançado"

83. O que é Markdown
    - O Markdown é uma forma de adicionar estilo a textos na web
    - O arquivo README.md aceita Markdown
    - Você vai conseguir exibir: Trechos de código, links, imagens e muito mais
    - Dando uma melhor experiência para o usuário nas suas documentações

84. Criando títulos
    - Os cabeçalhos em Markdown são determinados pelo símbolo `#`
    - Cabeçalhos são os famosos títulos ou heading do HTML
    - `#` = H1, `##` = H2, `###` = H3 e assim por diante

85. Ênfase nos textos
    - Temos símbolos que podem dar ênfase ao texto
    - Para escrever em negrito: `**TEXTO**` ou `__TEXTO__`
    - Para escrever em itálico: `*TEXTO*` ou `_TEXTO_`
    - Combinando os dois: _um **TEXTO** combinado_

86. Listas com Markdown
    - Temos as listas ordenadas e não ordenadas em Markdown
    - As listas não ordenadas começam os ítens com: `* Item` ou `- Item`
    - As listas ordenadas com: `1. Item`

87. Inserindo imagens
    - É possível inserir imagens em Markdown também
    - Veja a sintaxe: `![Texto](Link da imagem)`
        - Imagem local: ![Luffy Local](/UDEMY-GIT-GITHUB/Class/img/luffy.png)
        - Imagem externa: ![Luffy Externo](https://www.google.com/url?sa=i&url=https%3A%2F%2Fanimerant.com.br%2Fanime-manga%2Fone-piece-o-riso-do-gear-5-de-luffy-nao-e-apenas-comedia-e-o-seu-crescimento-pessoal%2F&psig=AOvVaw0PW6aBaXQM-JNXOCjhB9mA&ust=1706903826547000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCOjp4LP2ioQDFQAAAAAdAAAAABAE) 
        
    - A imagem pode estar no próprio repo ou ser externa

88. Links em Markdown
    - 