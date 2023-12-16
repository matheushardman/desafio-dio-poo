# Desafio de Projeto - Abstraindo um Bootcamp Usando Orientação a Objetos em Java

Repositório designado para o desafio de projeto do módulo "Programação Orientada a Objetos com Java" do Bootcamp Banco PAN JAVA Developer com objetivo de aplicar os conceitos estudados em POO

## Sobre o desafio

O desafio consiste em abstrair o domínio Bootcamp, criando classes que representem os assuntos relacionados ao mesmo, como os cursos e mentorias, o desenvolvedor que irá realiza-lo e o próprio bootcamp. 

Para isso criou-se seis (6) classes ao total, Conteudo, Curso, Mentoria, Dev, Bootcamp e Main.

Neste desafio utilizou-se os conceitos dos pilares do Paradigma de Programação Orientada a Objetos (POO): Abstração, Encapsulamento, Polimorfismo e Herança.

### Classe Conteudo

Utilizou-se o pilar Herança da POO para criar uma classe Conteudo que tem atributos característicos tanto das classes Curso quanto Mentoria, esses atributos são titulo e mentoria, além disso define-se o atributo XP_PADRAO como final recebendo o valor de 10. O método presente nessa classe é o calcularXp que foi sobrescrito nas classes Curso e Mentoria.

[Código Classe Conteudo](https://github.com/matheushardman/desafio-dio-poo/blob/main/src/br/com/dio/desafio/dominio/Conteudo.java)

### Classe Curso

A classe Curso herda os atributos da classe Conteudo e adiciona um atributo próprio (cargaHoraria), além de sobrescrever o método calcularXp, multiplicando a XP_PADRAO pela cargaHoraria.

[Código Classe Curso](https://github.com/matheushardman/desafio-dio-poo/blob/main/src/br/com/dio/desafio/dominio/Curso.java)

### Classe Mentoria

A classe Mentoria herda os atributos da classe Conteudo e adiciona um atributo próprio (data) que utiliza a classe LocalDate, além de sobrescrever o método calcularXp, somando 20 pontos ao XP_PADRAO para cada mentoria finalizada.

[Código Classe Mentoria](https://github.com/matheushardman/desafio-dio-poo/blob/main/src/br/com/dio/desafio/dominio/Mentoria.java)

### Classe Bootcamp

Para essa classe os atributos são nome, descrição, dataInicial, dataFinal (utilizando a classe LocalDate), devsInscritos (HashSet) e conteudos (LinkedHashSet) para representar o bootcamp.

[Código Classe Bootcamp](https://github.com/matheushardman/desafio-dio-poo/blob/main/src/br/com/dio/desafio/dominio/Bootcamp.java)

### Classe Dev

Nessa classe definiu-se os atributos nome, conteúdos inscritos e concluídos esses dois últimos através da Interface Set (Polimorfismo utilizando o LinkedHashSet). Os métodos nessa classe foram criados para inscrever o desenvolvedor no bootcamp, realizar a progressão do mesmo com a conclusão dos conteúdos, além de calcular a XP acumulada no bootcamp.

[Código Classe Dev](https://github.com/matheushardman/desafio-dio-poo/blob/main/src/br/com/dio/desafio/dominio/Dev.java)

### Classe Main

Na classe main, define-se os objetos com base nas classes Curso para adicionar um novo curso, Mentoria para adicionar uma nova mentoria, Bootcamp para adicionar um bootcamp e Dev para adicionar um desenvolvedor que fará o bootcamp.

[Código Classe Main](https://github.com/matheushardman/desafio-dio-poo/blob/main/src/Main.java)
