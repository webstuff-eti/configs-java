# configs-java
Arquivos de configurações de ambiente de desenvolvimento Java


Testando variáveis de ambiente:

1 - JAVA_HOME: No prompt do DOS entre com o seguinte comando: javac -version
  - Resultado esperado:     javac 1.8.0_201
  
  - -- Definição:
    É o diretório raiz de instalação do Java, quando necessário, executa ou compila um programa (IDE/ linhas de comando MAVEN).
  
2 - JRE_HOME: No prompt do DOS entre com o seguinte comando:  java -version
  - Resultado esperado:     java version "1.8.0_201"
							Java(TM) SE Runtime Environment (build 1.8.0_201-b09)
							Java HotSpot(TM) 64-Bit Server VM (build 25.201-b09, mixed mode)
							
3 - M2_HOME: No prompt do DOS entre com o seguinte comando: mvn -v 
  - Resultado esperado:   	Java HotSpot(TM) 64-Bit Server VM warning: ignoring option MaxPermSize=1024m; support was removed in 8.0
							Apache Maven 3.6.1 (xxxxxxxxxxx)
							Maven home: C:\apache-maven-3.6.1\bin\..
							Java version: 1.8.0_201, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk1.8.0_201\jre
							Default locale: pt_BR, platform encoding: Cp1252
							OS name: "windows 10", version: "10.0", arch: "amd64", family: "windows"
							
4 - MAVEN_HOME: No prompt do DOS entre com o seguinte comando: mvn -version 
  - Resultado esperado:	 idem ao item anterior

    Importante! Como algumas ferramentas de software fazem uso vezes da váriável M2_HOME, vezes MAVEN_HOME, logo para evitar problemas
                futuro, eu opto sempre em criar as 2.	
				
5 - MAVEN_OPTS:  Por padrão o Maven assumira uma alocação máxima de heap de 512 MB iniciando com 256 MB, logo através da criação da variável,
				 nos possibilitar aumentar o valor padrão.
				 
				Possiveis problemas: 
				 
					java.lang.OutOfMemoryError-> ocorre sempre que uma aplicação em seu momento de BUILD, seja necessários maisque 512 MB de heap.
				 
    Para saber mais e em detalhes:
    Link disponível em: <https://www.infoq.com/br/articles/Java-PERMGEN-Removed>25/04/2019
	
6 - CLASSPATH: 
            -- Definição: Caminho de classe, responsável em indicar os .jars que estão localizados na pasta lib e jre/lib do JDK.
	
				