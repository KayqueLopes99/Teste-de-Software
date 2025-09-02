## Conceitualização
### Conceito e termos de teste
| Termo                | Conceito Técnico                                                               | Explicação Simples                                                     | Exemplo                                                        |
| -------------------- | ------------------------------------------------------------------------------ | ---------------------------------------------------------------------- | -------------------------------------------------------------- |
| **Engano (mistake)** | Ação humana incorreta durante análise, design ou codificação.                  | É o **erro humano** (o programador ou analista faz algo errado).       | Programador esquece de validar um campo obrigatório.           |
| **Defeito (fault)**  | Anomalia estática em um artefato de software (código, documentação, process), ou seja, definição de dados incorretos. | O engano vira um **defeito no código ou processo**.                    | Condição `if` escrita de forma incorreta.                      |
| **Erro (error)**     | Estado interno incorreto ou inesperado em tempo de execução.                   | Quando o sistema roda, o defeito gera um **estado interno incorreto**. | Variável recebe valor negativo onde só era permitido positivo. |
| **Falha (failure)**  | Desvio do comportamento externo em relação aos requisitos especificados.       | O erro interno aparece para o usuário como **comportamento errado**.   | Botão não envia o formulário.                                  |

- Linha de causa e efeito:
**Engano (humano) ➝ Defeito (código/processo) ➝ Erro (interno) ➝ Falha (externa visível).**

- A falha é algo visível ao usuário do software/sistema.
- O defeito é uma imperfeição ou deficiência em um produto no qual ele não atende os seus requisitos ou especificações. Podem assimilar a falta.

> Falta: O resultado / representação de um erro

> Uma falta de comissão ocorre quando nós inserimos algo na representação que está incorreto

> Faltas de omissão ocorrem quando nós falhamos em inserir informação correta

> Bug: Trata-se do resultado de um erro de código (anomalia)














## Validação & Verificação (IEEE)
- Validação : O processo de avaliar o software no final do
desenvolvimento para garantir a conformidade com o uso
pretendido
> Estamos construindo o software correto?
> Garantir que o software atende as expectativas do cliente (usuário)

- Verificação : O processo de determinar se os produtos de
uma determinada fase do processo de desenvolvimento de
software atendem aos requisitos estabelecidos durante a
fase anterior
> Estamos construindo o software corretamente?
> Checar se o software satisfaz os seus requisitos funcionais e não-funcionais

#### Termos:
> Teste : Processo de avaliar o software ao observar sua execução.
> Falha de Teste : Execução de um teste que resulta em uma falha de software.
> Depuração (debugging) : O processo de encontrar um defeito dada uma falha.

- Modelo de Defeito & Falha (RIPR)
> 0.1 - Alcançabilidade (Reachability).
> 0.2 - Infecção (Infection).
> 0.3 - Propagação (Propagation).
> 0.4 - Revelabilidade (Revealability).

### Níveis de teste (OO):
- Teste Intraclasse: Testa uma classe inteira a partir da chamada de seus métodos em sequência.
- Teste Interclasse: Testa múltiplas classes juntas.
- Teste Intermétodo: Testa pares de métodos na mesma classe 
- Teste Intramétodo: Testa cada método individualmente

### Critérios de Cobertura
- Fornecem maneiras práticas e estruturadas de pesquisar o espaço de entrada. 

> Critério de teste: são as regras gerais que definem como o teste deve ser feito. Ex.: testar todas as instruções do código ou cobrir todos os requisitos funcionais.

> Requisitos de teste: são os itens específicos que precisam ser verificados. Ex.: cada linha de código pode virar um requisito de teste; cada requisito funcional também pode virar um requisito de teste.

### Tipos de teste: 
> Teste Funcional (caixa-preta): olha de fora, baseado em requisitos e especificações. Não importa o código, só se a função faz o que deveria (descrições externas do software).
> Teste Estrutural (caixa-branca): olha por dentro, baseado no código. Testa instruções, condicionais e fluxos internos.
> Teste Baseado em Modelos: olha os modelos de representação do sistema (ex.: UML). Os testes vêm desses modelos.

Funcional = foco no que o software deve fazer.
Estrutural = foco em como o código funciona internamente.
Baseado em Modelos = foco na representação/modelo do sistema.

- **Projeto de Testes**: é escolher **valores de entrada** que realmente testem o software.

- Atividades principais:

- 1. **Projeto de Testes**

   * **(a) Baseado em Critérios**: gera valores para cumprir regras de cobertura (ex.: todas as instruções).
   * **(b) Baseado em Conhecimento Humano**: usa experiência e conhecimento do domínio para criar valores de teste.

- 2. **Automação de Testes**: transforma os valores de teste em scripts automáticos.

   > Quanto maior a automação, menos gente precisa executar manualmente.

- 3. **Execução de Testes**: roda os testes no software e coleta resultados.

- 4. **Avaliação de Testes**: analisa os resultados e repassa para os desenvolvedores.

- **Outras atividades**: gerenciamento, manutenção e documentação de testes.

* **Projeto** = definir valores de teste.
* **Automação** = transformar em scripts.
* **Execução** = rodar testes.
* **Avaliação** = analisar resultados.

- **MDTD**: método que ajuda o projetista a calcular e garantir critérios de cobertura nos testes.



---
![](image\image1.png)

---


## Fases de Teste de Software
O processo de teste deve abranger desde **testes de baixo nível** (verificação de pequenos trechos de código) até **testes de alto nível** (validação de funcionalidades de acordo com os requisitos do cliente).

---
![](image\image.png)

---

## 🔹 0.1 Teste de Unidade
* Cada **unidade do sistema** (módulo, classe, função) é testada isoladamente.
* Objetivo: garantir que a unidade funciona conforme especificado.
* **Limitação**: não garante o funcionamento correto quando integrada a outras unidades.
* Desafio: difícil prever todos os casos especiais de entrada.
> Teste Unitário (teste do desenvolvedor) : Testa cada unidade (método) individualmente.


---

## 🔹 0.2 Teste de Integração

* Verifica a **interação entre as unidades** do sistema.
* Objetivo: identificar falhas na **troca de dados** entre módulos.
* **Não inclui**: integração com sistemas externos.
> Testa como módulos interagem um com outro.
---

## 🔹 0.3 Teste de Aceitação / Validação

* Conduzido por **usuários finais** ou representantes do cliente.
* Simula operações reais do sistema.
* Objetivo: confirmar se o software atende aos **requisitos do cliente**.
* É um **teste formal**, que define se o cliente aceita ou não o sistema.
* Pode usar **dados reais** ou **cenários específicos**.
> O software é aceitável para o usuário?

---

## 🔹 0.4 Teste de Sistema

* O sistema é testado como um **todo**, do ponto de vista do **usuário final**.
* Verifica se todas as funcionalidades funcionam de forma integrada.
* Inclui checagem de desempenho e comportamento global do sistema.
> Testa a funcionalidade geral do sistema.
---

## 🔹 0.5 Teste de Regressão

* Aplicado em **novas versões** do software ou em novos ciclos de teste.
* Repete os testes anteriores para garantir que **mudanças não quebraram** funcionalidades já existentes.
* Geralmente é **automatizado**.

---

## Percurso Resumido

1. **Unidade** → testar cada componente isolado.
2. **Integração** → verificar a comunicação entre componentes.
3. **Validação (Aceitação)** → garantir que o software atende aos requisitos.
4. **Sistema** → verificar o funcionamento completo e integrado.
5. **Regressão** → confirmar que versões novas não causaram falhas antigas.

---
