# Github - Udemy

## Introdução e instalação das dependências

Aula 1: Introdução
- Introdução ao que aprenderemos durante o curso, comandos e conceitos sobre Git e GitHub.

Aula 2: Apresentação do curso
- Apresentação de como foi separadas as seções e de que forma iremos aprender.

Aula 3: Instalando o Git no Windows
- Instalando git via chocolatey: `choco install git` ou instalando baixando o executável nesse link <https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git>

Aula 4: Instalando o Git no Linux
- Só utilizar o melhor gerenciador de pacotes, como o YUM `sudo yum install git-all` ou APT `sudo apt-get install git-all` seguindo esse link: <https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git>

Aula 5: Instalando o VS Code no Windowns
- Instalando o VS Code, baixar o executável nesse link <https://code.visualstudio.com/download>

Aula 6: Instalando o VS Code no Linux
- Instalando o VS Code, baixar o melhor executável nesse link <https://code.visualstudio.com/download>

Aula 7: O que é controle de versão
- Uma técnica que ajuda a gerenciar o código-fonte de uma aplicação;
- Registrando todas as modificações de código, podendo também reverter as mesmas;
- Criar versões de um software em diferentes estágios, podendo alterar facilmente entre elas;
- Cada membro da equipe pode trabalhar em uma versão diferente;
- Há ferramentas para trabalhar o controle de versão com GIT e SVN.

Aula 8: O que é Git
- O sistema de controle de versão mais utilizado no mundo atualmente;
- O Git é baseado em repositórios, que contêm todas as versões do código e também  as cópias de cada desenvolvedor;
- Todas as operações do Git são otimizadas para ter alto desempenho;
- Todos os objetos do Git são protegidos com criptografia para evitar alterações indevidas e maliciosas;
- O Git é um projeto de código aberto

Aula 9: Como tirar o máximo de proveito do curso
- Codificar junto
- Criar exemplos
- Criar outros casos usando os exemplos passados
- Ouvir e depois praticar

Aula 10: Slides do curso
- Arquivo PDF com os slides do curso.

Aula 11: Link do repositório do portfólio
- <https://github.com/matheusbattisti/matheusbattisti.github.io>

Aula 12: Indicações de livros
- Livro: <https://amzn.to/3ULsWwH>

Aula 13: Conclusão da primeira seção
- Conclusão da introdução e da instalação das principais dependências.

## Git fundamental

Aula 14: Introdução da seção
- Iremos aprender comandos fundamentais do Git

Aula 15: O que é um repositório
- Onde o código será armazenado;
- Na maioria das vezes cada projeto tem um repositório;
- Quando criamos um repositório estamos iniciando um projeto;
- O repositório pode ir para servidores que são especializados em gerenciar repos, como GitHub e BitBucket;
- Cada um dos desenvolvedores do time pode baixar o repositório e criar versões diferentes em sua máquina.

Aula 16: Criando um repositório
- Para criar um repositório utilizamos o comando `git init`
- Desta maneira o git vai criar os arquivos necessários para inicializa-lo;
- Que estão na pasta oculta `.git`
- Após este comando o diretório atual será reconhecido pelo git como um projeto e responderá aos seus demais comandos.
- Comandos:
    - `git status` para verificar se existe um repositório ativo
    - `git init` para iniciar um projeto de um diretório.

Aula 17: O que é GitHub
- É um serviço para gerenciar repositórios, gratuito e amplamente utilizado;
- Podemos enviar nossos projetos para o GitHub e disponibiliza-lo para outros devs;
- O GitHub é gratuito tanto para projetos públicos como privados;
- Criando uma conta no <https://github.com/>

Aula 18: Mudança do nome principal de branch
- Alteração de alguns anos atrás da branch principal de `master` para `main`

Aula 19: Enviando repositórios para o GitHub
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

Aula 20: Verificando alterações
- As mudanças do projeto podem ser verificadas por `git status`
    - Existem arquivos modificados que aparecem como `Modified` e novos arquivo que aparecem como `Untracked`
- Este comando é utilizado frequentemente;
- Aqui serão mapeadas todas as alterações do projeto;
- Como: arquivos não monitorados e arquivos modificados;
- Podemos também dizer que é a diferença do que já está enviado ao servidor ou salvo no projeto

Aula 21: Adicionando arquivos ao projeto
- Para adicionar arquivos a um projeto utilizamos `git add`
- Podemos adicionar um arquivo especifico como também diversos de uma só vez;
    - `git add NOMEDOARQUIVO` adicionando um arquivo especifico
    - `git add .` adicionando todos os arquivos modificos de uma vez.
- Somente adicionando arquivos eles serão "monitorados" pelo git;
- Ou seja, se não adicionar ele não estará no controle de versão;
- É interessante utilizar este comando de tempos em tempos para não perder algo por descuido.

Aula 22: Salvando alterações
- As alterações salvas do projeto são realizadas por `git commit`
- Podemos commitar arquivos especificos ou vários de uma vez com a flag `-a`
    - `git commit NOMEDOARQUIVO -m "MENSAGEM"` "commita" um único arquivo.
    - `git commit -a -m "MENSAGEM"` para "commitar" todos os arquivos, sem a flag `-a` também funciona commitar todos os arquivos.
- É uma boa prática enviar uma mensagem a cada commit, com as alterações que foram realizadas;
- A mensagem pode ser adicionada com a flag `-m`

Aula 23: Enviando código para o repositório
- Quando finalizamos uma funcionalidade nova, enviamos o código ao repo remoto, que é o código-fonte;
- Esta ação é feita pelo `git push` (Estamos trabalhando diretamente na main/master)
- Após esta ação o código do servidor será utilizado baseando-se no código local enviado

Aula 24: Recebendo alterações
- É comum também ter que sincronizar o local com as mudanças do remoto;
- Esta ação é feito por `git pull`
- Após o comando serão buscadas atualizações, se encontradas elas serão unidas ao código atual existente na nossa máquinas.

Aula 25: Clonando repositórios
- O ato de baixar um repositório de um servidor remoto é chamado de clonar repositório;
- Para esta ação utilizamos `git clone LINKDOREPOSITORIO .` (para pegar o link, só ir no site do GitHub, ir na opção `Code` e copiar o link).
- Passando a referência do repositório remoto;
- Este comando é utilizado quando entramos em um novo projeto, por exemplo.

Aula 26: Removendo arquivos
- Os arquivos podem ser deletados da monitoração do Git;
- O comando para deletar é `git rm`
- Após deletar um arquivo do Git ele não terá mais suas atualizações consideradas pelo Git;
- Apenas quando for adicionado novamente pelo `git add`

Aula 27: Verificando as alterações por meio de log
- Podemos acessar um log de modificações feitas no projeto;
- O comando para este recurso é `git log`
- Você receberá uma informação dos commits realizados no projeto até então.

Aula 28: Renomeando arquivos
- Com o comando `git mv` podemos renomear um arquivo;
- O mesmo também pode ser removido para outra pasta;
- E isso fará com que este novo arquivo seja monitorado pelo Git;
- O arquivo anterior é excluído.

Aula 29: Desfazendo operações
- O arquivo modificado pode ser retornado ao seu estado original;
- O comando utilizado é o `git checkout NOMEDOARQUIVO` (volta o estado original do arquivo)
- Após a utilização do mesmo o arquivo sai do staging;
- Caso seja feita uma próxima alteração ele entra em staging novamente

Aula 30: Ignorando arquivos e diretórios em um projeto
- Uma técnica muito utilizada é ignorar arquivos do projeto;
- Devemos inserir um arquivo chamado `.gitignore` na raiz do projeto;
- Nele podemos inserir todos os arquivos que não devem entrar no versionamento;
- Isso é útil para arquivos gerados automaticamente ou arquivos que contêm informações sensiveis

Aula 31: Resetando um branch
- Com o comando `git reset` podemos resetar as mudanças feitas
- Geralmente é utilizado com a flag `--hard`
- Comando: `git reset --hard origin/NOMEDABRANCH` faz com que reset a branch atual deixando no mesmo estado que está na branch que você aponte.
- Todas as alterações "commitadas" e também as pendentes serão excluídas

Aula 32: Conclusão da seção
- Concluindo seção com comandos fundamentais do Git.

Teste 1: Quiz sobre os comandos fundamentais
- Contém 4 perguntas, 100% de acerto

## Trabalhando com Branches

Aula 33: Introdução sobre a seção
- Introdução breve do que aprenderemos na seção "trabalhando com branches"

Aula 34: O que são Branches
- Branch é uma forma que o Git separa as versões dos projetos;
- Quando um projeto é criado ele inicia na branch `main`, estamos trabalhando nela até este ponto do curso;
- Geralmente cada nova feature de um projeto fica em uma branch separada;
- Após a finalização das alterações os branches são unidos para ter o código-fonte final

Aula 35: criando e visualizando branches
- Para visualizar os branches disponíveis basta digitar `git branch`
- Para cria um branch você precisa utilizar o comando `git branch NOMEPARABRANCH`
- Estas duas operações são muito utilizadas no dia a dia de um dev

Aula 36: Deletando branches
- Podemos deletar um branch com a flg `-d` ou `--delete`
- Comando: `git branch -d NOMEDABRANCH`
- Não é comum deletar um branch, normalmente guardamos o histórico do trabalho;
- Geralmente se usa o delete quando o branch foi criado errado

Aula 37: Mudando de branch
- Podemos mudar para outro branch utilizando o comando `git checkout -b NOMEDABRANCH` (esse comando muda de branch já criando um novo)
- Esta comando também é utilizado para dispensar mudanças de um arquivo
- Alterando o branch podemos levar alterações que não foram commitadas junto, tome cuidado

Aula 38: Unindo branches
- O código de dois branches distintos pode ser unido pelo comando `git merge NOMEDABRANCH`
- Outro comando para a lista dos mais utilizados
- Normalmente é por meio dele que recebemos as atualizações de outros devs

Aula 39: Utilizando a stach
- 