# Java
TED5 da Disciplina Linguagem de Programação 2 do curso de Sistemas para Internet do Uniesp.

Professora: Alana Morais

ENUNCIADO

Implemente as seguintes classes:

Classe Cachorro

Possui os atributos nome, raça, sexo (M ou F), idade, energia e numero_filhotes. Os dois últimos atributos não são passados por parâmetro pelo construtor, pois são sempre inicializados dentro dele. Energia sempre é inicializada com 100 e numero_filhotes sempre é inicializado com 0. Não esqueça os gets e sets.

Método toString(): retorna uma string com as informações dos 6 atributos.

Método comer(comida): o cachorro só pode comer se a energia estiver de 50 para baixo. (i) O cão pode comer três tipos diferentes de comida, de acordo com o parâmetro passado. (ii) A comida R (de ração) aumenta sua energia em 50. (iii) A comida C (de carne) aumenta sua energia em 40. (iv) A comida L (de legumes) aumenta sua energia em 30. Independentemente do que for passado como parâmetro, esse método sempre retorna a energia atual do cão.

Método brincar(brincadeira): o cachorro só pode brincar se a energia estiver de 40 para cima. (i) O cão pode ter três tipos diferentes de brincadeira, de acordo com o parâmetro passado. (ii) A brincadeira B (de buscar bolinha) diminui sua energia em 30. (iii) A brincadeira S (de saltar) diminui sua energia em 20. (iv) A brincadeira G (de girar pelo chão) diminui sua energia em 10. Independentemente do que for passado como parâmetro, esse método também sempre retorna a energia atual do cão.

Método pode_cruzar(parc): Esse método define se o cão pode cruzar com o(a) parceiro(a) passado como parâmetro. Para isso, checa as seguintes condições: (i) Ambos os cães precisam ter entre 1 e 9 anos. (ii) Ambos os cães precisam ser da mesma raça. (iii) Ambos os cães precisam estar com energia mínima de 80. (iv) Os cães precisam ser de sexo diferentes. Se todas as condições acima forem satisfeitas, o método retorna Verdadeiro. Do contrário retorna Falso.

Método cruzar(parc): Primeiramente verifica se o cruzamento entre o cão atual e o cão parc é válido. Se for, diminui a energia de ambos em 50. Além disso, o código deve gerar um número aleatório de filhotes entre 3 e 10, e atualizar o atributo numero_filhotes de ambos os cães. O método retorna o número de filhotes gerado pelo cruzamento.

Classe Casa

Possui duas funções: main() e manipular_cachorro(cao_atual, lista_caes).

A) Função main(): Exibe o menu inicial com as opções:       1) Cadastrar cão;       2) Listar cães e       3) Sair do programa.  

Quando o usuário escolhe a opção 3, o programa deve ser encerrado usando a função exit(0) do pacote sys. 

Quando o usuário escolhe a opção 1, o programa deve pedir para o usuário cadastrar nome, raça, sexo e idade do cão. Um objeto Cachorro é criado com essas informações e esse objeto é inserido numa lista de cães. O programa volta ao menu inicial. 

Quando o usuário escolhe a opção 2, o programa deve exibir a lista de cães cadastrados, para que o usuário escolha um cão para manipular. 

Quando o usuário selecionar um cão, deve ser chamada a função manipular_cachorro(), passando como parâmetros o cão selecionado e a lista de cães cadastrados.

B) Função manipular_cachorro(cao_atual, lista_caes): Exibe um menu com as opções: 1) Ver dados do cão; 2) Alimentar; 3) Brincar; 4) Cruzar; 5) Menu Inicial.

Quando o usuário escolhe a opção 5, o programa volta para o menu inicial.

Quando o usuário escolhe a opção 1, o programa exibe as informações do cão atual, chamando o método obter_dados() e exibindo-o numa mensagem.

Quando o usuário escolhe a opção 2, o programa verifica se é necessário o cão comer, através do nível de sua energia. Se o cão estiver com energia em até 50, o programa exibe três opções de alimento para o cão: ração, carne ou legumes. Por fim, exibe qual é o nível de energia do cão após se alimentar, utilizando o método comer(comida). Então retorna ao menu de manipulação.

Quando o usuário escolhe a opção 3, o programa verifica se é possível o cão brincar, através do nível de sua energia. Se o cão estiver com energia de 40 para mais, o programa exibe três opções de brincadeira para o cão: buscar bolinha, saltar ou girar. Por fim, exibe qual é o nível de energia do cão após brincar, utilizando o método brincar(brincadeira). Retorna ao menu de manipulação.

Quando o usuário escolhe a opção 4, o programa exibe uma lista somente com os(as) parceiros(as) possíveis de cruzar com o cão naquele momento (pode ser feito usando o método pode_cruzar(parc)). Após selecionar a parceria para o cruzamento, o programa chama o método cruzar(parc) e exibe quantos filhotes foram gerados desse cruzamento.
Em qualquer menu ou submenu não devem ser aceitas entradas diferentes das opções exibidas.
