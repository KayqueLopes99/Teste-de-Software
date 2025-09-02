## Termos Tipos de Teste
- Casos de teste: 
- A especificação deve ser concreta e clara o suficiente para desenvolvermos casos de teste.
- Desse modo, determinar um conjunto de casos de teste para o item a ser testado é a essência do teste de software.
> Um caso de teste completo irá conter um identificador do caso de teste, uma breve declaração de seu propósito, uma descrição das precondições, as entradas reais do caso de teste, os resultados esperados, uma descrição das pós-condições esperadas e um histórico de execução.

- Ele terá dois resultados: `PASS` e `FAIL`.
- Como saber se o resultado de teste está correto?
- Ex: 
````
No SIGAA há um módulo para o cálculo das médias dos alunos
Você vai testar este módulo
Assumindo que ninguém tira notas menores que 0 é esperado que qualquer teste produza uma média maior ou igual a 0
Além disso, dado o domínio de médias, é sabido que elas serão em um intervalo conhecido
Eventualmente, conseguimos determinar um oráculo com base no nosso conhecimento do domínio do problema que estamos testando
````

## Necessidades:
- É preciso estabelecer as precondições necessárias (entradas para os casos de teste), observar os resultados (comparar isto com o oráculo) e garantir que as pós-condições esperadas existem para determinar se o teste passou.

> Critérios:
- Conscistência: Deve haver clareza no relacionamento caso de teste e  especificações que o caso de teste exercita.
- 

```
Considerando o problema de testar o módulo de cálculo de médias do SIGAA, faz sentido todos os casos de teste passarem entradas de notas menores que zero?
É importante que o caso de teste seja elaborado em conformidade com a especificação do sistema a ser testado
```

> Tamanho
- Depende o $.
- Para cada caso de teste: devemos descrever as condições necessárias para o teste (precondições)
- Oraculo de teste (resultados esperados). 
- Ao executarmos o teste, verificamos o seu resultado e, com base no oráculo, ele passou ou falhou


### Teste suíte:
Um conjunto de casos de teste a serem executados em um ciclo específico de testes.

## Tipos de teste:
> Teste caixa branca - visão interna - detalhe procedimental - Os caminhos lógicos do software 
- Baseado na estrutura interna do software
- Testa fluxos de controle, dados, loops, etc.
- 1. exercitar a lógica interna e as interfaces de todos os componentes do software.
- (2) Conhecendo o funcionamento interno de um produto, podem ser realizados testes para assegurar que "tudo se encaixa" - que as operações internas foram realizadas de acordo com as especificações e que todos os componentes internos foram adequadamente exercitados



#### Porblema o numero de caminho pode ser enorme. 
> **Também chamado de teste da caixa-de-vidro, é uma filosofia de projeto de casos de teste que usa o texto do programa (código) para derivar casos de teste**
- testa caminhos
- exercitam decisões lógicas TRUE e FALSE.
- exercitam ciclos e limites.
- exercitam estruturas de dados internas.
- fluxo do objeto.
- Aplica-se: testes de componentes e testes de integração
- cada parte do código deve ser executa pelo menos uma vez.
- os resultados esperados devem ser determinados usando os requisitos ou especificações, não o código.

#### Abordagens:
- Teste do caminho básico.
- Teste de condição.
- este de fluxo de dados.
- Teste de ciclo.

> Teste caixa preta - visão externa - interface do software

- Baseado em requisitos e especificações
- Testa funcionalidades, usabilidade, desempenho, etc.
- 2. exercitar os domínios de entrada/saída do programa para descobrir erros no funcionamento, comportamento e desempenho do programa.
- (1) Conhecendo a função especificada para o qual um produto foi projetado para realizar, podem ser feitos testes que demonstram que cada uma das funções é totalmente operacional, embora ao mesmo tempo procurem erros em cada função.
- Também chamado de teste comportamental, teste baseado em requisitos/especificações.

- Busca encontrar erros nas seguintes categorias:
- (1) funções incorretas ou faltando
- (2) erros de interface
- (3) erros em estruturas de dados ou acesso a bases de dados externas
- (4) erros de comportamento ou de desempenho
- (5) erros de inicialização e término
> Abordagens 
- Partição de equivalência: divide o domínio de entrada em classes de equivalência.

```` md
É uma forma de testar um programa **sem olhar o código por dentro**.
Você só testa **de fora**, como se fosse um usuário comum.

- **Você só se importa com:**

* O que você coloca no sistema (**entrada**)
* O que ele te devolve (**saída**)

Não importa **como ele faz** lá dentro.

- Exemplo 
* Um **calculador online**:

  * Você digita `2 + 2` → espera `4`.
  * Você digita `2 / 0` → espera mensagem de erro.


- Resumo: 
* **Teste de Caixa Preta = Testar de fora**
* **Entra dado → Sai resultado**
* **Não olha o código, só verifica se funciona como deveria**

````
> Teste baseado em modelos: usa informações contidas no modelo de requisitos como base para a geração de casos de teste.

### **Testes daixa cinza:**
- Trata-se de testes que combinam características de testes caixa-branca e caixa-preta.



#### Um bom teste tem alta probabilidade de encontrar um erro
- Ideia: Teste de regressão: este teste é realizado após a realização de uma melhoria ou um reparo no programa.

