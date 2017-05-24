<img align="right"
src="https://seeklogo.com/images/U/UFMG-logo-7B1478CE80-seeklogo.com.gif" style="width: 150px"/>

<h6> UNIVERSIDADE FEDERAL DE MINAS GERAIS</h6>
<h6> INSTITUTO DE CIÊNCIAS EXATAS</h6>
<h6> DEPARTAMENTO DE CIÊNCIA DA COMPUTAÇÃO</h6>
<h6> ENGENHARIA DE SOFTWARE II</h6>

<h3>Trabalho Prático 1 - APACHE CASSANDRA</h3>

<h5> Participantes:</h5>

* Beatriz Lana
* Guilherme Viegas
* Lorena Cerbino

<h3>Descrição do Sistema</h3>

<p align="justify">
O sistema <b>Apache Cassandra</b> é um sistema de banco de dados <b>NoSQL</b> distribuído,de código aberto, altamente escalável e de alto desempenho do Apache, feito para gerenciar quantidades enormes de dados estruturados. Por ser escalável, fornece grande disponibilidade e nenhum ponto de falha.
</p>

> <p align="justify">Um banco de dados <b>NoSQL</b> (<i>Not Only SQL</i>, ou Não Somente SQL) é um banco de dados não-relacional que não segue as propriedades <b>ACID</b> (atomicidade, consistência, isolamento e durabilidade). Bancos <b>NoSQL</b> oferecem escalabilidade horizontal, que substituem o modelo relacional ao armazenar os dados em colunas, não exigem esquemas de tabela fixa e não costumam suportar instruções de junção SQL. Este tipo de banco de dados não possue esquema, suportam replicação, tem API simples e tem capacidade para lidar com enormes quantidades de dados, provendo simplicidade de projeto e controle mais fino sobre a disponibilidade.</p>

> <center><img style="width: 700px" src="https://teddyma.gitbooks.io/learncassandra/content/assets/sortedmap.jpg"/></center>

> <h4>Banco de Dados Relacional x NoSQL</h4>

> Banco de dados Relacional    | Banco de dados NoSQL
> ---                 | ---
> Suporta linguagem de consulta poderosa    | Suporta linguagem de consulta simples
> Possui esquema fixo    | Não possui esquema fixo
> Segue as propriedades <b>ACID</b> |    Apenas "eventualmente consistente"
> Suporta transações    | Não suporta transações

> <p align="justify">Entre os bancos de dados <b>NoSQL</b> populares estão Apache HBase e MongoDB.</p>

> <center><img style="width: 700px" src="https://blog.appdynamics.com/wp-content/uploads/2011/06/Screen-shot-2011-06-29-at-3.41.01-PM.png"/></center>

<p align="justify">
Criado no <b>Facebook</b>, o <b>Cassandra</b> é bastante diferente dos sistemas de gerenciamento de banco de dados relacional, visto que é um banco de dados orientado a colunas. Seu objetivo é lidar com grandes quantidades de dados, usando o sistema distribuído par-a-par (p2p) através dos nós para distribuir os dados entre todos os nós em um <i>cluster</i>. Seu design de distribuição e replicação é baseado no sistema <b>Dynamo</b>, da <b>Amazon</b>, sem nenhum ponto de falha e adicionando um modelo de dados de "conjunto de colunas" mais poderoso, baseado no <b>Google Bigtable</b>.
</p>

<center><img style="border: 20px solid transparent" width="500px" src="https://image.slidesharecdn.com/ceanoverviewofcassandra-111110155159-phpapp02/95/an-overview-of-apache-cassandra-4-728.jpg?cb=1320999379"/></center>

<p align="justify">
Todos os nós de um <i>cluster</i> devem desempenhar o mesmo papel, sendo independentes e interconectados entre eles. Cada nó pode aceitar solicitações de leitura e de gravação, independentemente de onde os dados estejam no <i>cluster</i>. Quando um nó cai os outros nós da rede podem prover os serviços de leitura e escrita.
</p>

<p align="justify">
O <b>Cassandra</b> foi desenvolvido no <b>Facebook</b> para a pesquisa na caixa de entrada, tornando-se <i>open-source</i> em Julho de 2008. Foi aceito na <b>Incubadora Apache</b> em Março de 2009, tornando-se um projeto de alto nível desde Fevereiro de 2010.
</p>

<p align="justify">
O <b>Apache Cassandra</b> está sendo usado por algumas das maiores empresas, tais como <b>Facebook</b>, <b>Twitter</b>, <b>Cisco</b>, <b>Rackspace</b>, <b>ebay</b> e <b>Netflix</b>. O motivo de tamanha adoção é visto nas características do banco de dados, apontadas a seguir.
</p>

<h4>Características Principais</h4>

* <p align="justify">O <b>Apache Cassandra</b> é <b>descentralizado</b>, ou seja, cada nó exerce a mesma função. Não há pontos de falha, os dados são distribuídos através do <i>cluster</i> para que, assim, cada nó possua dados diferentes e possa atender a qualquer pedido, tornando o banco de dados continuamente disponível para aplicações críticas de negócios.</p>

<center><img src="https://blogs.mulesoft.com/wp-content/uploads/2013/09/cassandra.blog_.2.png"/></center>

* <p align="justify">Este banco de dados também suporta <b>replicação</b>, oferecendo flexibilidade de distribuir dados onde precisa. O <b>Apache Cassandra</b> é  idealizado como um sistema distribuído para permitir a implantação de um grande número de nós em diversos <i>data centers</i> , sendo que as características de sua arquitetura são adaptadas para a implantação de múltiplos <i>data centers</i>, para a redundância e para a prevenção e recuperação contra possíveis desastres. Também é permitido escolher entre usar replicação síncrona ou assíncrona.</p>

<center><img src="http://www.w3ii.com/cassandra/data_replication.jpg"/></center>

* <p align="justify">A <b>escalabilidade elástica</b> do <b>Cassandra</b> pode ser vista através do tempo de processamento de leitura e escrita, que aumenta sua taxa de transferência de forma linear de acordo com o acréscimo de hardware para acomodação de novos clientes e mais dados, sem que haja tempo de inatividade nem a interrupção de aplicativos, mantendo o tempo de resposta rápido.</p>

* <p align="justify">O <b>Apache Cassandra</b> é <b>tolerante a falhas</b>. Os dados são copiados para vários nós para tolerância a falhas, o que é suportado pelo banco, além do fato de que os nós com falha podem ser substituídos sem tempo de inatividade.</p>

* <p align="justify">O <b>Cassandra</b> também permite que leituras e escritas ofereçam um <b>nível ajustável de consistência</b>.</p>

<img align="right" style="border-left: 20px solid transparent" src="https://opencredo.com/wp-content/uploads/2016/08/cassandra-overview-400x233.jpg"/>

* <p align="justify">O banco de dados tem integração com o <b>Hadoop</b>, com suporte a <i>MapReduce</i>, além de possuir também suporte para <b>Apache Pig</b> e <b>Apache Hive</b>.</p>

* <p align="justify">O <b>Apache Cassandra</b> foi desenvolvido na plataforma <b>Java</b> e introduziu a linguagem de consulta <i>Cassandra Query Language (CQL)</i>, que é uma interface simples para acessar o banco de dados em alternativa à tradicional <i>Structured Query Language (SQL)</i>. A <b>CQL</b> acrescenta uma camada de abstração que encapsula detalhes de implementação dessa estrutura, fornecendo sintaxes nativas para coleções e outras codificações comuns, disponíveis para as linguagens <b>Java (JDBC)</b>, <b>Python (DBAPI12)</b>, <b>Node.Js (Helenus)</b>, <b>Go (gocql)</b> e <b>C++</b>.</p>

* <p align="justify"><b>Cassandra</b> pode acomodar todos os formatos de dados possíveis, ou seja, estruturado, semi-estruturado e não estruturado e pode acomodar dinamicamente as alterações estruturais de acordo com a necessidade.</p>

*  <p align="justify">Por último, o <b>Cassandra</b> possui suporte a transações, portanto suporta as propriedades de Atomicidade, Consistência, Isolamento e Durabilidade (ACID)</p>

<h6>Comparação entre modelo relacional e o banco de dados <b>Cassandra</b>:</h6>

<center><img src="https://teddyma.gitbooks.io/learncassandra/content/assets/analogy.jpg"/></center>

<h3>Informações da Equipe de Desenvolvimento</h3>

<p align="justify">A principal organização responsável pelo desenvolvimento do <b>Cassandra</b> é a <i>Apache Software Foundation</i>, que atualmente é dona do banco de dados. No <i>GitHub</i>, os principais desenvolvedores do <b>Apache Cassandra</b> nos últimos anos são os perfis de <b>Jonathan Ellis</b>, <b>Sylvain Lebresne</b> e <b>Brandon Williams</b>, com seus respectivos números de contribuições bastante significativos. São 4.526, 1.611 e 1.200 commits respectivamente desde o lançamento da primeira versão do <b>Apache Cassandra</b>, incluindo tanto as referentes à manutenção de erros quanto ao lançamento de novas funcionalidades e versões completas.</p>

<p align="justify"><b>Jonathan Ellis</b> é, além do usuário mais ativo no desenvolvimento e atualização do <b>Cassandra</b>, o atual presidente do projeto na <i>Apache</i>. A principal função dele na <i>Apache Software Foundation</i> é comunicar aos diretores o andamento do projeto <b>Apache Cassandra</b>, bem como decisões que foram tomadas pelo comitê de gerenciamento de projetos.</p>

<p align="justify"><b>Sylvain Lebresne</b> é um desenvolvedor que começou utilizando e contribuindo para o <b>Cassandra</b>. Hoje em dia ele também faz parte do comitê de gerenciamento de projetos na <i>Apache</i> e trabalha diretamente para o projeto, desenvolvendo em tempo integral para o mesmo.</p>

<p align="justify">Os autores originais do projeto <b>Cassandra</b> são <b>Avinash Lakshman</b> e <b>Prashant Malik</b>, que iniciaram o desenvolvimento do banco de dados no <b>Facebook</b>, com o intuito de otimizar a ferramenta de busca de mensagens. O programa foi, então, lançado no mês de Julho de 2008 com código <i>open source</i> pelo próprio <b>Facebook</b>. Pouco tempo depois o projeto se tornou propriedade da <i>Apache</i>, sendo até hoje considerado um banco de dados muito bom, com atualizações constantes e grande escalabilidade.</p>

<p align="justify">O código do <b>Cassandra</b> é até hoje <i>open source</i>, vários desenvolvedores de todas as partes do mundo colaboram com seu desenvolvimento e atualização. Os colaboradores mais frequentes e que atuam mais ativamente no desenvolvimento são por volta de seis desenvolvedores, entretanto, quase 200 desenvolvedores já contribuíram de alguma forma para o <b>Cassandra</b>, atuando principalmente para consertar algum problema específico que tiveram durante a utilização do banco de dados. Outra tarefa recorrente é a comunicação de erros, para que sejam resolvidos por outros desenvolvedores da comunidade do <b>Cassandra</b>.</p>

<h3>Evolução do Sistema</h3>

<p align="justify">O <b>Apache Cassandra</b> está se aproximando de um processo de lançamento mensal, denominado Tick-Tock. Cada nova atualização numerada com um número par (<i>ex. 3.2</i>) contém acréscimo de ferramentas; já as atualizações ímpares (<i>ex. 3.3</i>) contém apenas correções de erros.</p>

<p align="justify">O último lançamento disponibilizado foi a atualização <b>3.10</b>, que foi liberada no dia 3 de fevereiro de 2017.</p>

<p align="justify">Algumas versões antigas continuam sendo suportadas, são elas:</p>

* <p align="justify"><b>Apache Cassandra 3.0</b>, que será suportado até que a versão <b>4.0</b>, sem data de lançamento determinada, complete 6 meses. A última atualização desta versão foi a de número <b>3.0.13</b>, disponibilizada para uso em 14 de abril de 2017.</p>

* <p align="justify"><b>Apache Cassandra 2.2</b>, que será suportado até  que a versão <b>4.0</b>, sem data de lançamento determinada, seja disponibilizada. A última atualização desta versão foi a de número <b>2.2.9</b>, disponibilizada para uso em 2 de fevereiro de 2017.</p>

* <p align="justify"><b>Apache Cassandra 2.1</b>, que será suportado até que a versão <b>4.0</b>, sem data de lançamento determinada, seja disponibilizada, sofrendo até lá apenas correções críticas. A última atualização desta versão foi a de número <b>2.1.17</b>, disponibilizada para uso em 2 de fevereiro de 2017.</p>

<h4>Histórico de Últimas Atualizações </h4>

<p align="justify">Versão <b>3.4.5</b>: </p>

- <p align="justify">Foi acrescentado o suporte a operadores matemáticos.</p>

- <p align="justify">Acréscimo de suporte para os operadores `+` e `-` em datas.</p> 

- <p align="justify">Acréscimo das funções `currentTimestamp`, `currentDate`, `currentTime` e `currentTimeUUID`.</p>

<p align="justify">Versão <b>3.4.4</b>: </p>

- <p align="justify">No comando `ALTER TABLE`, o operador `ALTER` foi removido.</p>

- <p align="justify">No comando `ALTER TYPE`, o operador `ALTER` foi removido.</p>

<p align="justify">Versão <b>3.4.3</b>: </p>

- <p align="justify">Acréscimo do novo tipo `DURATION`.</p>

- <p align="justify">Foi adicionado o suporte para o operador `GROUP BY`.</p>

- <p align="justify">Adição da opção `DEFAULT UNSET` para a operação `INSERT JSON`, que permite ignorar colunas omitidas.</p>

- <p align="justify">O operador `null` passa a ser um valor válido para TTL em um `INSERT` ou `UPDATE`, e que é equivalente a inserir um valor 0. </p>

<p align="justify">Versão <b>3.4.2</b>: </p>

- <p align="justify">Os comandos `ALTER TABLE`, `ADD` e `DROP` passam a estar disponíveis para a adicição e removeção de múltiplas colunas.</p>

- <p align="justify">Acréscimo da opção `PER PARTITION LIMIT` na cláusula `SELECT`.</p>

- <p align="justify">As funções definidas pelo usuário passam a poder instanciar `UDTValue` e `TupleValue`  através da nova interface `UDFContext`.</p>

<p align="justify">Versão <b>3.4.1</b>: </p>

- <p align="justify">Acréscimo de funções para `CAST`.</p>

<p align="justify">Versão <b>3.4.0</b>: </p>

- <p align="justify">Acréscimo de suporte para <i>views</i> materializadas.</p>

<p align="justify">Versão <b>3.3.1</b>: </p>

- <p align="justify">A sintaxe `TRUNCATE TABLE X` passa a ser aceita como um <i>alias</i> para `TRUNCATE X`.</p>

<p align="justify">Versão <b>3.3.0</b>: </p>

- <p align="justify">Adição de suporte para a criação de funções definidas pelo usuário. </p>

- <p align="justify">Adição dos novos tipos `date`, `time`, `tinyint` e `smallint`. </p>

- <p align="justify">Acréscimo de suporte a `JSON`.</p>

- <p align="justify">Foram adicionadas novas funções para a conversão de tempo, que tornam as funções `dateOf` e `unixTimestampOf` obsoletas. </p>

<p align="justify">Versão <b>3.2.0</b>: </p>

- <p align="justify">Adição de suporte aos tipos que são criados pelo usuário.</p>

- <p align="justify">A operação `CREATE INDEX` passa a suportar a indexação de <i>collection columns</i>, incluindo a indexação das <i>keys</i> por meio da função `keys( )`.</p>

- <p align="justify">Os índices de coleção passam a poder ser consultados através dos operadores `CONTAINS` e `CONTAINS KEY`.</p>

- <p align="justify">O tipo de dados dupla foi adicionado. </p>

<p align="justify">Versão <b>3.1.7</b>: </p>

- <p align="justify">A instrução`SELECT` passa a suportar a seleção de várias linhas em uma única partição, utilizando a cláusula `IN`em uma combinação de <i>clustering columns</i>. </p>

- <p align="justify">As sintaxes de `IF EXISTS` e `IF NOT EXISTS` passam a ser suportadas pelas instruções `CREATE USER` e `DROP USER`, respectivamente. </p>

<p align="justify">Versão <b>3.1.6</b>: </p>

- <p align="justify">Um novo método <b>uuid()</b> foi adicionado.</p>

- <p align="justify">Suporte para a sintaxe `DELETE ... IF EXISTS`.</p>

<p align="justify">Versão <b>3.1.5</b>: </p>

- <p align="justify">Torna-se possível o agrupamento das colunas de um cluster em uma relação.</p>

- <p align="justify">Foi Adicionado o suporte para colunas estáticas. </p>

<p align="justify">Versão <b>3.1.4</b>: </p>

- <p align="justify">A operação `CREATE INDEX` passa a permitir especificar opções ao criar índices personalizados `CUSTOM`.</p>

<p align="justify">Versão <b>3.1.3</b>:</p>

- <p align="justify">O <i>timestamp parser</i> passa a funcionar com precisão de milissegundos. </p>

<p align="justify">Versão <b>3.1.2</b>:</p>

- <p align="justify">As palavras `NaN` e `Infinity` eram constantes flutuantes válidas. A partir desta versão, tornam-se palavras reservadas. No caso improvável de seu uso como identificador de tabela, será necessário dobrá-las. </p>


<p align="justify">Versão <b>3.1.1</b>:</p>

- <p align="justify">A instrução `SELECT` passa a permitir listar as chaves de partição (<i>partition keys</i>) ao utilizar o modificador `DISTINCT`.</p>

- <p align="justify">A sintaxe `c IN ?` passa a ser suportada na cláusula `WHERE`. Nesse caso, o valor de retorno esperado será uma lista de qualquer tipo de c. </p>

<p align="justify">Versão <b>3.1.0</b>:</p>

- <p align="justify">Foi adicionada a operação `ALTER TABLE DROP`. </p>

- <p align="justify">A instrução `SELECT` passa a aceitar <i>alias</i> na cláusula <i>select</i>, contudo o <i>alias</i> ainda não é suportado nas instruções `WHERE` e `ORDER BY`.</p>

- <p align="justify">As instruções `CREATE`, `KEYSPACE`, `TABLE` e `INDEX` passam a suportar a condição `IF NOT EXISTS`. Similarmente, a instrução `DROP` passa a suportar a condição `IF EXISTS`.</p>

- <p align="justify">Opcionalmente, a instrução `INSERT` passa a suportar a condição `IF NOT EXISTS` e a instrução `UPDATE` à condição `IF`. </p>

<p align="justify">Versão <b>3.0.5</b>:</p>

- <p align="justify">As instruções `SELECT`, `UPDATE` e `DELETE` passam a aceitar agora a cláusula `IN` vazia. </p>

<p align="justify">Versão <b>3.0.4</b>:</p>

- <p align="justify">Foi atualizada a sintaxe para índices secundários personalizados.</p>

- <p align="justify">A condição diferente passa a não ser suportada para a <i>partition key</i>.</p>

<p align="justify">Versão <b>3.0.3</b>:</p>

- <p align="justify">Foi adicionado o suporte para os índices secundários personalizados.</p>

<p align="justify">Versão <b>3.0.2</b>:</p>

- <p align="justify">A validação de tipo para constantes foi corrigida, passando a ser agora mais rigorosa e restrita, por exemplo, para os tipos <i>int</i> e <i>blob</i>. </p>

- <p align="justify">A correção feita anteriormente levou à introdução de um novo tipo de constante <i>blob</i>, que permite a entrada de dados do tipo <i>blob (basic large object)</i>. Observe que, embora a entrada de <i>blobs</i> como <i>strings</i> ainda seja suportada por esta versão (para permitir uma transição mais suave para <i>blob</i> constante ), ela se encontra desativada e será removida em uma versão futura. Se você estava usando <i>strings</i> como <i>blobs</i>, é necessário atualizar seu código de cliente o mais rápido possível para alternar as constantes de <i>blob</i>.</p>

- <p align="justify">Também foram introduzidas várias funções para converter tipos nativos em <i>blobs</i>. Além disso, a função <i>token</i> também passa a ser permitida em cláusulas `select`.</p>

<p align="justify">Versão <b>3.0.1</b>:</p>

- <p align="justify"><i>Data strings</i> (assim como <i>timestamps</i>) passam a não serem aceitos como valores válidos para <b>timeuuid</b>. Considerá-lo consistia em um erro, tendo em vista que <i>data string</i> não é um <b>timeuuid</b> válido, e, sendo assim, resultava em um comportamento confuso e/ou conflituoso. No entanto, os seguintes novos métodos foram adcionados para auxiliar o trabalho com <b>timeuuid</b>: <i>minTimeuuid</i>, <i>maxTimeuuid</i>, <i>dateOf</i> e <i>unixTimestampOf</i>.</p>

- <p align="justify">As constantes flutuantes passam a suportar a notação de expoente. Em outras palavras, 4.2E10 é, agora, um valor de ponto flutuante válido.</p>

<h3>Principais Frameworks</h3>

<p align="justify">O <b>Apache Cassandra</b> foi desenvolvido em <b>Java</b> e é um sistema multiplataforma. A escolha da linguagem <b>Java</b> para tal tarefa provavelmente se dá por razões como segurança, performance, portabilidade e capacidade de otimização. Em relação a segurança, pode-se afirmar que é relativamente fácil desenvolver um código seguro em <b>Java</b> quando em comparação a outras linguagens, como <b>C/C++</b> por exemplo. Isso porque <b>Java</b> possui formas de encapsular o código que não são visíveis ao programador (manipulação de endereços de memória, por exemplo), o que também acaba minimizando bastante os possíveis erros do desenvolvedor. A performance do <b>Java</b>, apesar de muitas vezes questionada por diversos desenvolvedores, possui uma referência muito boa. Primeiramente porque a performance em <b>Java</b> pode ser um problema no momento do desenvolvimento em si, mas quando o programa é finalizado seu comportamento é melhor que em outras linguagens. Além disso, por ser amplamente utilizado, há atualizações constantes da linguagem, além de muitas informações a respeito na internet, em livros, artigos, etc. Além disso, como o <b>Cassandra</b> surgiu com a ideia de ser multiplataforma, o <b>Java</b> se mostra a melhor opção, pois tem a constante preocupação em desenvolver serviços multiplataforma e, preferencialmente, que funcionem exatamente da mesma maneira em todos os ambientes. Finalmente, <b>Java</b> usa uma ferramenta <i>just-in-time (JIT)</i> que é capaz de fazer otimizações de performance e aumentar sua velocidade consideravelmente.</p>
 
<p align="justify">A maioria dos <i>frameworks</i> e APIs ligados ao <b>Cassandra</b> utilizam-no para criar outras interfaces. Um exemplo é o <b>Datastax Java Driver para Apache Cassandra</b>, que é um cliente <b>Java</b> associado ao <i>Datastax Enterprise</i> que utiliza o protocolo e a linguagem do banco de dados <b>Cassandra</b>. Com ele é possível fazer a integração de um cliente <b>Java</b> com o banco de dados referido.</p>

<p align="justify">Um outro <i>framework</i> muito utilizado é o <b>Mesos Cassandra</b>, uma integração do <b>Apache Mesos</b> com o <b>Apache Cassandra</b>. O <b>Apache Mesos</b> é um kernel de sistemas distribuídos que foi desenvolvido com o mesmo princípio do kernel do Linux, porém em proporções diferentes. Sua principal tarefa é isolar recursos e compartilhá-los através de aplicações distribuídas ou outros <i>frameworks</i>, ficando entre o sistema operacional e a aplicação. Em outras palavras, ele facilita o gerenciamento de aplicações em larga escala. Aliado ao <b>Apache Cassandra</b>, é possível facilitar e automatizar tarefas que normalmente seriam executadas à mão por desenvolvedores ao implementar o <b>Apache Mesos</b>. Isso ocorria com bastante frequência, pelo fato de o <b>Apache Mesos</b> ser uma ferramenta de larga escala e diversas vezes precisar de um banco de dados robusto, que pudesse operar em larga escala também. Pensando nisso, o <i>framework</i> <b>Mesos Cassandra</b> foi desenvolvido para sanar as necessidades de aliar um kernel de sistemas distribuídos em larga escala com um banco de dados escalável e que opera bem também em larga escala.</p>

<h3>Arquitetura</h3>

<p align="justify">O <b>Cassandra</b> foi desenvolvido tendo em vista que problemas de <i>hardware</i> e <i>software</i> podem e de fato ocorrem. Sendo assim, o sistema foi pensado de forma que os dados sejam distribuídos ao longo de vários nós independentes e interligados uns aos outros.</p>

<p align="justify">Cada nó do <i>cluster</i> pode aceitar pedidos de leitura e escrita independentemente de onde os dados estejam de fato armazenados e, caso um nó torne-se indisponível, solicitações de leitura e escrita podem ser atendidas por outros nós da rede. Através da chave, o nó que atendeu a uma requisição consegue rastrear e saber quais nós do <i>cluster</i> possuem informações do dado desejado.  O sistema então aguarda até que um <i>quorum</i> de nós responda com o dado, no caso da leitura, ou responda com uma confirmação, no caso de uma escrita. </p>

<p align="justify">Os nós de um <i>cluster</i> no <b> Apache Cassandra</b> são organizados de forma cíclica, o que torna mais fácil a adição e remoção de nós no <i>cluster</i>. Quando um nó é adicionado ao <i>cluster</i> somente seus vizinhos são afetados. Cada nó possui um intervalo de valores determinados. Os dados são, então, divididos entre os nós baseando-se no <i>hashing</i> da chave identificadora de determinado dado. O <i>hash</i> gera um valor que é então designado a um determinado nó, o que depende do intervalo de valor do mesmo. A máquina responsável por determinado dado é chamada de coordenadora.</p>

<center><img src="https://www.ibm.com/developerworks/br/library/os-apache-cassandra/figure003.gif"/></center>

<p align="justify">A replicação dos dados nos bancos <b>Cassandra</b> é utilizada para garantir uma alta disponibilidade dos dados. Cada dado é encontrado em N nós do <i>cluster</i>, onde esse N é um fator configurável. Para escolher os N-1 nós onde o dado será replicado, existem três formas diferentes: <i>Rack Unaware</i>, <i>Rack Aware</i> e <i>Datacenter Aware</i>. No modo <i>Rack Unaware</i>, o coordenador simplesmente escolhe os N - 1 nós seguintes. Nos outros modos, é utilizado um sistema externo que elege um dos nós como líder para informar aos outros nós a faixa de valores do anel que ele será uma réplica.</p> 

### Referências 

http://cassandra.apache.org/
http://mesos.apache.org/
https://en.wikipedia.org/wiki/Apache_Cassandra
https://www.datastax.com
https://opensource.com/business/14/9/open-source-datacenter-computing-apache-mesos
http://www.dcomp.sor.ufscar.br/verdi/topicosCloud/Cassandra.pdf
https://www.ibm.com/developerworks/br/library/os-apache-cassandra/
https://stackoverflow.com/questions/2341866/why-was-cassandra-written-in-java
