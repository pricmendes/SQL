# Correção na Procedure PROC_APONTAMENTO

## 🛠️ Problema Identificado

Na análise da procedure `PROC_APONTAMENTO`, foi constatada uma falha na atualização do saldo produzido na tabela `ORDEM_PROD`. Adicionalmente, a situação dos registros não era alterada para "F" (finalizado) conforme o esperado.

## 📝 Solução Implementada

Para resolver essa questão, as seguintes modificações foram realizadas:

- **Reposicionamento do Condicional `IF`:** O condicional responsável pela atualização do saldo e da situação foi realocado para a posição correta dentro da lógica da procedure.
- **Tratamento de Valores `NULL` na Coluna `QTD_PROD`:** Foram efetuadas alterações em todas as ocorrências onde a coluna `QTD_PROD` apresentava o valor `NULL`, garantindo o correto fluxo de atualização.
- **Fechamento de Cursores:** Todos os cursores que permaneciam abertos foram devidamente fechados, visando a otimização do desempenho da procedure e a prevenção de potenciais problemas de recursos.

## 📸 Evidências Visuais

| Descrição | Demonstração |
| :--- | :--- |
| **Erro do Cursor Aberto:** <br> Demonstra o problema de um cursor não sendo fechado corretamente. | <a href="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PRINT1.png"><img src="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PRINT1.png" width="150"></a> |
| **Execução da Procedure com Erro:** <br> Apresenta a execução da procedure antes da correção, evidenciando o problema. | <a href="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PRINT2.png"><img src="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PRINT2.png" width="150"></a> |
| **Resultado com Erro:** <br> Ilustra o resultado incorreto da procedure antes da implementação da solução. | <a href="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PRINT3.png"><img src="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PRINT3.png" width="150"></a> |
| **Tabela `ORDEM_PROD` com Valores `NULL`:** <br> Exibe a situação da tabela onde a coluna `QTD_PROD` continha valores `NULL`, impedindo a atualização. | <a href="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/QTD_PROD.png"><img src="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/QTD_PROD.png" width="150"></a> |
| **Resultado Final Corrigido:** <br> Apresenta o resultado da procedure após as modificações, demonstrando a correção do problema. | <a href="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PROCEDURE_CORRETA.jpg"><img src="https://raw.githubusercontent.com/pricmendes/SQL/refs/heads/main/imagens/PROCEDURE_CORRETA.jpg" width="150"></a> |

*💡 Clique nas imagens para ampliar e visualizar os detalhes.*

## 🔗 Link para a Solução

Para uma análise mais detalhada da solução implementada, acesse o seguinte link:

[Link para a Solução](https://github.com/pricmendes/SQL/blob/main/PROC_APONTAMENTO)
