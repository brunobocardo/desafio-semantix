# desafio-semantix
Desafio Engenheiro de Dados - Semantix


# Respostas das questões:

i) Qual o objetivo do comando cache em Spark
R: Alocar os arquivos na memória

ii) O mesmo código implementado em Spark é normalmente mais rápido que a implementação equivalente em MapReduce. Por quê?
R: Porque o Spark executa o processamento em memória, não fazendo escrita e leitura em disco como o MapReduce.

iii) Qual é a função do SparkContext?
R: A função do SparkContext é permitir que a aplicação acesse os Clusters com ajuda do Resource Manager.

iv)Explique com suas palavras o que é Resilient Distrubuted Datasets(RDD).
R: RDD é coleção de registros que podem vir de qualquer fonte de dados, sendo o RDD, imutável, distribuido e resilientes armazenadas em um ou mais nós em um cluster.
O acesso aos dados é feito por API's que permite interar sobre eles.

v)GroupByKey é menos eficiente que reduceByKey em grandes dataset. Por quê?
R: No reduceByKey, os dados não são embaralhados no início e a função de redução pode ser aplicada na mesma partição, já no GroupByKey,
os dados das partições são embaralhados na rede para forma de cada chave tem uma lista de valores.
Quando o dataset é muito grande, o trabalho de agregar chaves e para cada chave, agregar os valores torna-se muito custoso.

vi)Explique o que o código Scala abaixo faz.
'''
val textFile = sc.textFile("hdfs://...")
val counts = textFile.flatMap(line => line.split(" "))
.map(word => (word, 1))
.reduceByKey(_ + _)
counts.saveAsTextFile("hdfs://...")
'''

R: Abre o arquivo texto e "splita" por espaço e cria um lista de 1 linha com todas as palavras.
Conta cada palavra na lista e depois reduz para contar as palavras unicas.
Salva o arquivo com a contagem das palavras.




# Respostas das quetões do desafio:

1)Número de hosts únicos?







2)O total de erros 404?








3)Os 5 URLs que mais causaram erro 404?








4)Quantidade de erros 404 por dia?








5)O total de bytes retornados?
