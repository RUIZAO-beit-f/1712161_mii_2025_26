Relatório do Trabalho prático
Programação I

Gestão de Viagens/Transportes



Aluno: Rui, 1712161, 
https://github.com/RUIZAO-beit-f, tgei222314@ensiguarda.com

 Indice
1. Descrição do Trabalho	3
2. Implementação do Trabalho	3
3. Funcionamento do trabalho	4
Entrada no programa	4
Recolha dos dados	4
Gravação da viagem	4
Repetição ou fim	5
8. Conclusão	5
Bibliografia	5

1-Descrição do Trabalho
O trabalho consiste no desenvolvimento de uma aplicação em linguagem C para apoio à gestão de viagens e transportes de clientes. O programa permite registar a informação básica do cliente e todos os dados relacionados com as diferentes etapas da viagem (planeamento, transporte, documentação, execução e avaliação final).​
A principal finalidade é aplicar conceitos de programação estruturada, nomeadamente utilização de struct, manipulação de ficheiros e organização dos dados em tabelas lógicas. Pretende‑se também aproximar o exercício de uma situação real de gestão de viagens, em que é necessário recolher, organizar e guardar informação de forma persistente.

2-Implementação do Trabalho	
  A implementação foi feita em C, utilizando o Visual Studio Code como ambiente de desenvolvimento e o compilador GCC para gerar o executável. Foi definida uma única estrutura Viagem, que reúne num só registo todos os campos do cliente e das etapas da viagem, simplificando o código e o armazenamento da informação.​
Foram criadas três funções principais:
lerString, responsável por ler texto do utilizador de forma segura;
registarViagem, que apresenta as perguntas ao utilizador e preenche todos os campos da struct;
guardarViagemFicheiro, que escreve os dados da viagem num ficheiro de texto (viagens.txt) em modo de acrescento, garantindo a persistência da informação.​
O programa principal (main) controla um ciclo que permite o registo de várias viagens consecutivas, perguntando no final se o utilizador pretende inserir um novo cliente.

3-Funcionamento do trabalho	
Ao iniciar o programa, o utilizador é guiado por um conjunto de perguntas organizadas por secções: dados do cliente, planeamento, transporte, documentação/compliance, execução lógica e acompanhamento/avaliação. Cada resposta é imediatamente gravada nos campos correspondentes da struct Viagem.​
Depois de concluído o preenchimento, a função guardarViagemFicheiro abre o ficheiro viagens.txt e escreve, de forma formatada, todos os dados introduzidos. Caso o utilizador decida registar outra viagem, o processo repete‑se e os novos 
registos são acrescentados ao fim do mesmo ficheiro, permitindo criar uma espécie de base de dados sequencial de viagens.​

Entrada no programa
O programa começa no main e cria uma variável do tipo Viagem (onde vai guardar tudo) e uma variável continuar para saber se o utilizador quer registar mais viagens.
Depois entra num ciclo while que só acaba quando respondes n.
Recolha dos dados
Dentro do ciclo chama a função que faz as perguntas (registarViagem na versão anterior, ou o próprio main na versão simplificada):
Primeiro pede nome e NIF do cliente.
Depois vai passando pelas etapas do teu diagrama: planeamento, transporte, documentação, execução e acompanhamento, sempre com printf a mostrar a pergunta e lerStr/scanf a guardar a resposta nos campos da struct.
No fim desta parte, tens a struct Viagem completamente preenchida com todas as respostas que o cliente deu.
Gravação da viagem
Logo a seguir, abre o ficheiro viagens.txt em modo de acrescentar ("a").
Escreve numa linha todos os campos da struct (por exemplo separados por ;) com fprintf, e fecha o ficheiro.
Isto significa: cada vez que preenches uma viagem, essa viagem fica registada no ficheiro, sem apagar as anteriores.

Repetição ou fim
Depois de gravar, o programa pergunta se queres inserir outra viagem.
Se escreveres s, o ciclo volta ao início: volta a perguntar tudo e volta a gravar mais uma linha no ficheiro.
Se escreveres n, sai do ciclo e mostra uma mensagem de fim de programa.
Resumindo o tópico 3 em linguagem simples:
O programa pergunta tudo ao utilizador,
Guarda as respostas numa struct,
Escreve essa struct num ficheiro,
E repete estes passos enquanto o utilizador quiser.

4-Conclusão
O trabalho permitiu consolidar vários conteúdos da disciplina, em particular a definição e utilização de struct, a interação com o utilizador através de leitura de dados e a escrita em ficheiros de texto. A organização dos campos segundo as etapas do diagrama de gestão de viagens ajudou a perceber a importância de planear a estrutura de dados antes de programar.​
Como melhoria futura, seria possível adicionar funcionalidades como pesquisa de viagens já registadas, alteração de dados, remoção lógica de registos ou gravação em ficheiro binário para maior eficiência. Também poderia ser criada uma interface mais amigável, com menus e validação mais rigorosa dos dados inseridos.​

5-Bibliografia
Material de apoio da disciplina de Programação em C e fichas de exercícios fornecidas pelo docente.​
Artigos e exemplos sobre manipulação de ficheiros em C, consultados em recursos educativos online de programação.​
Tutoriais e documentação sobre configuração do compilador GCC e utilização do Visual Studio Code para desenvolvimento em C.​



