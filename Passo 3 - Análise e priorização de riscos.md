## 8. Análise e priorização de riscos

A análise de risco foi realizada a partir das ameaças identificadas com o STRIDE e dos casos de abuso descritos anteriormente.

Para cada risco, foram avaliados:

* o evento que pode causar prejuízo;
* a ameaça relacionada;
* a vulnerabilidade ou condição que permite o evento;
* a probabilidade de ocorrência;
* o impacto esperado;
* a pontuação e o nível de prioridade.

### 8.1 Critérios de probabilidade

| Valor | Classificação | Critério utilizado                                                                           |
| ----- | ------------- | -------------------------------------------------------------------------------------------- |
| 1     | Baixa         | O evento depende de condições incomuns, acesso muito específico ou grande capacidade técnica |
| 2     | Média-baixa   | O evento é possível, mas depende de uma vulnerabilidade ou condição específica               |
| 3     | Média-alta    | O evento é plausível e pode ocorrer em situações comuns de uso ou ataque                     |
| 4     | Alta          | O evento pode ocorrer com facilidade, frequência ou durante condições previsíveis do sistema |

### 8.2 Critérios de impacto

| Valor | Classificação | Critério utilizado                                                                   |
| ----- | ------------- | ------------------------------------------------------------------------------------ |
| 1     | Baixo         | Causa pequeno transtorno e pode ser corrigido rapidamente                            |
| 2     | Moderado      | Causa interrupção ou inconsistência limitada, com possibilidade de recuperação       |
| 3     | Alto          | Causa prejuízo acadêmico, administrativo ou exposição relevante de informações       |
| 4     | Muito alto    | Pode afetar muitos usuários, comprometer operações críticas ou causar prejuízo grave |

### 8.3 Cálculo e classificação

A pontuação de cada risco é calculada da seguinte forma:

`Pontuação = Probabilidade × Impacto`

| Pontuação | Nível do risco |
| --------- | -------------- |
| 1 a 3     | Baixo          |
| 4 a 7     | Médio          |
| 8 a 11    | Alto           |
| 12 a 16   | Crítico        |

A pontuação auxilia na comparação dos riscos, mas não substitui a justificativa e a análise do contexto.
