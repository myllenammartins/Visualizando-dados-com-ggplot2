# Visualizando-dados-com-ggplot2

Atividade prática: Visualizando dados com ggplot2.
Colocando em prática a atividade do curso Google Data Analytics: Análise de dados com programação em R.
#
## Visão geral da atividade
Essa atividade teve como objetivo conhecer a lógica básica da visualização de dados em ***ggplot2*** e aprender como criar um gráfico usando código R.

## Fundamentos de ggplot2
O pacote ggplot2 permite criar gráficos de alta qualidade e customizáveis com os seus dados. ***ggplot2*** baseia-se na gramática dos gráficos, que é um sistema para descrever e construir visualizações de dados. A ideia essencial por trás da gramática dos gráficos é que você pode criar qualquer gráfico a partir dos mesmos componentes básicos, como se fossem blocos de construir.

## Preparação dos dados
### Conjunto de dados escolhido
- Dados dos pinguins do arquipélago Palmer, foram levantados de 2007 a 2009 pela Dra. Kristen Gorman, membro do programa Palmer Station Long Term Ecological Research.

### Etapas
1. install.packages() para instalar o ggplot2 e o conjunto de dados de Palmer pinguins: install.packages(“ggplot2”) e install.packages(“palmerpenguins”)
2. Carregar o ggplot2 e o conjunto de dados usando a função library(): library(ggplot2) e library(palmerpenguins)
3. Examinar o data frame para os dados dos pinguins. Para isso, usei as funções data() e View(): data(penguins) e View(penguins)

Retornando o seguinte:

   ![Captura de tela 2023-11-23 092158](https://github.com/myllenammartins/Visualizando-dados-com-ggplot2/assets/99662544/fb1238c5-f9c2-4fa2-9192-6fe782ccc83d)

## Criando o gráfico em ggplot2
O objetivo foi criar um gráfico da relação entre massa corporal e comprimento da nadadeira nas três espécies de pinguim. Escolhi um geom específico que se encaixe no tipo de dados que tenho.
Os pontos mostram a relação entre duas variáveis quantitativas. Um diagrama de dispersão dos pontos seria uma maneira efetiva de mostrar a relação entre as duas variáveis. Coloquei o comprimento da nadadeira no eixo X e massa corporal no eixo Y.
Código utilizado para criar o gráfico: ggplot(data = penguins) +geom_point(mapping = aes(x = flipper_length_mm, y = body_mass_g))
- ***ggplot(data = penguins)***:Cria um sistema de coordenadas ao qual é possível acrescentar camadas.
- ***+***: Depois, acrescenta-se um símbolo “+” para adicionar uma nova camada ao seu gráfico. O gráfico é finalizado adicionando uma ou mais camadas ao ggplot().
- ***geom_point()***: A função geom_point() utiliza pontos para criar gráficos de dispersão.
- ***(mapping = aes(x = flipper_length_mm, y = body_mass_g))***: Cada função geom em ggplot2 leva um argumento de mapeamento. Com isso, define-se como as variáveis do conjunto de dados serão mapeadas de acordo com as propriedades visuais. O argumento de mapeamento sempre é combinado com a função aes(). Os argumentos x e y da função aes() especificam quais variáveis devem ser mapeadas no eixo X e no eixo Y do sistema de coordenadas. Neste caso, deseja-se mapear a variável “flipper_length_mm” no eixo X e a variável “body_mass_g” no eixo Y.

Obtendo o seguinte gráfico:

![Captura de tela 2023-11-23 092420](https://github.com/myllenammartins/Visualizando-dados-com-ggplot2/assets/99662544/51183aca-856e-4650-abd8-b395b47335cd)

***O gráfico mostra uma relação positiva entre as duas variáveis. Em outras palavras, quanto maior o pinguim, mais longa é a nadadeira.***

## Mapear a variável espécies com a estética cor
Atribuindo uma cor diferente para cada espécie de pinguim:

![Captura de tela 2023-11-23 141055](https://github.com/myllenammartins/Visualizando-dados-com-ggplot2/assets/99662544/5380e46f-4695-4b03-b956-a5eb5fb7595c)

