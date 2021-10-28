# **Grupo de Trabalho em Análise Estrutural**

Teste e Construção da Página do GTAE, a qual terá (?):


-   Download de arquivos e das matrizes que formos gerar, garantindo uma menor dependencia nossa frente a edições no site do GIC. <!--# Num quer dizer que vamos desistir do site do GIC, é só para termos uma maior versatilidade mesmo. -->

-   Links de Eventos Passados e Futuros do Grupo, bem como o material de apoio que formos gerar. Não só a escola de verão.

-   Informações de Contato. (?)

-   Calêndario de Eventos envolvendo membros do Grupo. (?)

-   Propaganda de outros produtos do grupo (como o pacote R).

-   Uma página falando sobre os cursos na pós envolvendo o grupo. (?)

A seguir vai estar indicado um guia para ações envolvendo o site, como mexer na página, como é a estrutura da página, como propagandear eventos do grupo, dar upload em dados para que fiquem disponíveis para dowload.
 
Link para acessar a página: https://analiseestrutural.github.io/GTAE.github.io/

O arquivo da página está no branch `gh_pages`.
  
<center> <h2> **Edição da Página** </h2> </center>

<center> <h2> **Estrutura da Página** </h2> </center>

<center> <h2> **Eventos** </h2> </center>

<center> <h2> **Estrutura na parte de Downloads** </h2> </center>

<center> <h2> **Estrutura na pasta Dados** </h2> </center>

Abaixo está exposto informações importantes para se ter em mente antes de dar um upload de uma base de dados na pasta `Dados/` (Sim, vamos manter as coisas mais ou menos arrumadas aqui).

No final da seção, tem um sumário com os pontos resumidos.

<center> <h4> **Arquivos para Referencias** </h4> </center>

-   Dentro da pasta `Dados/` existe uma pasta `Dados/referencias/` para abrigar todas as referências dos textos.

-   Dentro da pasta `Dados/referencias/` existem duas pastas: `PT/` e `EN/`. Como é de se imaginar, uma é para arquivos como se o texto fosse ser citado em português (`PT/`) e outra em inglês (`EN/`).

    Suponha o caso da citação abaixo:

    > PASSONI, Patieene A. Deindustrialization and regressive specialization in the Brazilian economy between 2000 and 2014: a critical assessment based on the input-output analysis. Tese (Doutorado em Economia da Indústria e da Tecnologia), Instituto de Economia, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2019. Disponível em: <http://objdig.ufrj.br/43/teses/PatieeneAlvesPassoni.pdf>

    Uma versão em inglês poderia ser algo como:

    > PASSONI, Patieene A. Deindustrialization and regressive specialization in the Brazilian economy between 2000 and 2014: a critical assessment based on the input-output analysis. Doctoral Thesis, Economics Institute, Federal University of Rio de Janeiro, 2019. Available at: <http://objdig.ufrj.br/43/teses/PatieeneAlvesPassoni.pdf>

    O objetivo é para o eventual leitor que não fala português ter condições de saber o que é cada coisa na citação. Não precisa estar perfeito num determinado estilo de citação (até porque existem vários). Apesar de improvável, o mesmo é válido para o caso contrário (do inglês para o português).

-   Esses arquivos serão nomeados indicando a lingua da citação, o texto, autor(es) e ano de publicação. No exemplo anteriormente temos então `Dados/referencias/EN/en_Thesis_Passoni_2019.txt` e `Dados/referencias/PT/pt_Tese_Passoni_2019.txt`.

-   Além da referência corrida em si, cada arquivo terá uma entrada de refêrencia `bibtex` como se fosse um arquivo `.bib`, que seja capaz de produzir aquela.

    -   Para quem não conhece, `bibtex` é uma forma para citação criada para o LaTeX, mas que hoje é suportada por outros programas como o [Word](https://interfacegroup.ch/how-can-i-use-my-bibtex-library-in-ms-word/). Exemplos de entradas `bibtex` podem ser encontrados aqui, aqui e por toda a internet. Detalhe, você verá aspas e colchetes como exemplos para cada elemento de uma entrada `bibtex`. De modo geral, **use colchetes.** Ou seja, ao invés de `year = "2019"` escreva `year = {2019}`.

    -   Se o texto a ser citado aparece no Google Scholar, mesmo se como **[CITAÇÃO]** apenas, uma forma fácil de pegar a entrada `.bib` é no botão Citar (que aparece como uma aspas) e então na "janela" que irá aparecer clique em `BibTeX` . A página então irá mostrar uma entrada `bibtex` para esse artigo. Nem sempre essa entrada `bibtex` do Google Scholar é perfeita, mas é de modo geral um bom ponto de partida.

-   A referência corrida deve estar toda numa linha do arquivo `.txt` (sem quebras de linha internas) Duas linhas depois terá escrito `%bibtex` indicado que a partir da linha abaixo é a entrada da referência em bibtex. No caso de `Dados/referencias/PT/pt_Tese_Passoni_2019.txt` o seu conteúdo é:

`PASSONI, Patieene A. Deindustrialization and regressive specialization in the Brazilian economy between 2000 and 2014: a critical assessment based on the input-output analysis. Tese (Doutorado em Economia da Indústria e da Tecnologia), Instituto de Economia, Universidade Federal do Rio de Janeiro, Rio de Janeiro, 2019. Disponível em: http://objdig.ufrj.br/43/teses/PatieeneAlvesPassoni.pdf`

`%Sugestão de bibtex (em portugues)`

`@phdthesis{passoni2019deindustrialization,`

`title={Deindustrialization and regressive specialization in the brazilia n economy between 2000 and 2014: a critical assessment based on the input-outpu t analysis},`

`author={Patieene Passoni},`

`school={Instituto de Economia, Universidade Federal do Rio de Janeiro, Rio de Janeiro},`

`year={2019},`

`type={Tese (Doutorado em Economia da Indústria e da Tecnologia)},`

`note={Disponível em http://objdig.ufrj.br/43/teses/PatieeneAlvesPassoni.pdf%7D`

`}`

<center> <h4> **Dados e Arquivos Comprimidos** </h4> </center>

-   **Comprima os arquivos em grupos** que fazem sentido (**leia** a seção sobre compressão de dados a seguir). Por exemplo, no caso dos arquivos dentro da pasta `MIP_42_PAA/`, ao invés de comprimir cada ano em separado comprima todos num zip só como você pode ver em `Dados/MIP_GIC/MIP_42_PAA.zip`. Quando as pessoas forem usar os dados, fará sentido imediato para elas os dados .

-   Dentro de todos os arquivos comprimidos, não irão apenas as bases de dados, mas também outros arquivos. Abaixo uma tabela com eles.

<center> <h6> Tabela 1: Arquivos para além da base de dados. </h6> </center>

|     |                     |                                                                                                                                                                     |                                                                             |           |
|:---:|:-------------------:|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|:---------:|
|  0  | `referencia_pt.txt` |                           Um arquivo `.txt` contendo a referência corrida e<br> a entrada `bibtex` como se estivesse escrita em português                           |                 **Obrigatório junto**<br> **à publicação**                  | Português |
|  0  | `reference_en.txt`  |                            Um arquivo `.txt` contendo a referência corrida e<br> a entrada `bibtex` como se estivesse escrita em inglês                             |                 **Obrigatório junto**<br> **à publicação**                  |  Inglês   |
|  1  |    `README.txt`     |                     Um arquivo `.txt` com informações básicas sobre os dados. <br>Também é valido colocar contato e avisar onde está a citação.                     |                          **Quase Imprescindível.**                          |  Inglês   |
|  1  |  `dataOutline.txt`  | Um arquivo `.txt` que seria como um índice de cada arquivo da base de dados. Pensem como a aba `ÍNDICE` das matrizes da Patieene. Indicar método de Deflação usado. | **Alta Importância**, <br>mas pode esperar ou<br>ser aprimorada com o tempo |  Inglês   |
|  2  |    `loadData.R`     |                        Um R script mostrando como ler o arquivo excel em todo os dados. De preferência, um que possa ser usado já do source.                        |                               Boas Práticas.                                |    \-     |
|  3  |  `exampleData.Rmd`  |                                                        Um arquivo `.Rmd` mostrando como ler e usar os dados.                                                        |                             Muita boa vontade.                              |  Inglês?  |

-   O ideal é que os arquivos tenham os nomes escrito ali em cima. Nesse caso, o arquivo `Dados/referencias/EN/en_Thesis_Passoni_2019.txt` seria apenas `reference_en.txt`. Tente criar os arquivos na ordem de preferência (quanto menor o número, mais urgente).

<center> <h4> **Compressão dos arquivos e tamanho dos arquivos.** </h4> </center>

-   **O github tem um limite de 100 megabytes (MB) por repositório.**

-   **Vá com calma na hora de formatar as planilhas.** Cores de fundo e coisa do gênero vão de pouco em pouco aumentando o tamanho do arquivo.

    -   Por via das dúvidas faça um teste criando uma versão com formatação e outra sem formatação para ver qual ocupa menos espaço. **Se a sem formatação for 1 MB menor que a com formatação, escolha ela.**

-   **É imperativo compactar** as bases de dados. **Dê prerência para o formato `.zip`** ao comprir. Ele não é o que melhor comprime, mas é facilmente manipulado pela maioria dos sistemas operacionais e programas de manipulação.

    -   **Não comprima de forma alguma(!)** os arquivos em `.7z` ou `tar.xz`, ou algum formato obscuro de compressão do tipo. Eles não tem fácil portabilidade para diferentes Sistemas Operacionais. E é um inferno para descomprimi-los via linha de comando ou código.

    -   **Evite** comprimir como `.rar`. Tente sempre usar o formato `.zip` mesmo.

    -   Não coloque senha na hora de comprimir.

-   Confira que não está esquecendo nenhum arquivo (ver Tabela 1)

<center> <h4> Sumário (Upload) </h4> </center>

-   Crie arquivos com as referências associadas à base de dados.

-   Vamos começar dando upload nos arquivos de Excel. **Use o formato o .zip para comprimir** grupos de arquivos que serão baixados de forma conjunta. **Não exagere** **na formatação** das planilhas.

-   Comprima os arquivos em grupos que fazem sentido. Além da base de dados, coloque também outros arquivos para auxiliar os usuários.
