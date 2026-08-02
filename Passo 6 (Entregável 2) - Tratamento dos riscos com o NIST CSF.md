

## 9. Tratamento dos riscos com o NIST CSF

Após a identificação e a priorização dos riscos, o grupo definiu estratégias e medidas para reduzir sua probabilidade ou seu impacto.

O NIST Cybersecurity Framework 2.0 foi utilizado para organizar os resultados de segurança esperados. O framework possui seis funções:

| Função | Finalidade no projeto |
| --- | --- |
| Govern | Definir políticas, responsabilidades, prioridades e critérios de aceitação de riscos |
| Identify | Conhecer os ativos, dependências, vulnerabilidades e riscos do sistema |
| Protect | Implementar salvaguardas para reduzir a probabilidade ou o impacto dos incidentes |
| Detect | Identificar eventos suspeitos, falhas e possíveis incidentes |
| Respond | Conter, analisar, comunicar e tratar incidentes detectados |
| Recover | Restaurar serviços e dados e reduzir os prejuízos causados |

As funções organizam os resultados esperados, mas não determinam uma tecnologia específica. Os controles apresentados a seguir são propostas do grupo para o sistema analisado.

### 9.1 Estratégias de tratamento

Foram consideradas quatro estratégias:

| Estratégia | Descrição |
| --- | --- |
| Evitar | Eliminar a atividade ou condição que dá origem ao risco |
| Reduzir | Implementar medidas para diminuir a probabilidade ou o impacto |
| Compartilhar | Atribuir parte da operação ou das consequências a um terceiro |
| Aceitar | Reconhecer e manter conscientemente o risco, com justificativa e acompanhamento |

A aceitação de um risco não significa ignorá-lo. A decisão deve ser justificada, aprovada por uma pessoa responsável e revisada quando o contexto mudar.

### 9.2 Estratégia escolhida para cada risco

| Risco | Nível inicial | Estratégia principal | Justificativa |
| --- | --- | --- | --- |
| R01 — Uso indevido da conta | Crítico | Reduzir | A funcionalidade de acesso remoto é necessária, mas pode receber proteções adicionais |
| R02 — Alteração indevida de dados | Alto | Reduzir | As operações acadêmicas precisam continuar disponíveis, com maior proteção de integridade |
| R03 — Negação de uma operação | Médio | Reduzir e aceitar o residual | Logs confiáveis reduzem o risco, mas não eliminam todas as possibilidades de contestação |
| R04 — Exposição de informações | Crítico | Reduzir | Os dados são necessários ao sistema, mas seu acesso deve ser limitado e monitorado |
| R05 — Indisponibilidade | Crítico | Reduzir e compartilhar | A universidade pode implementar proteções próprias e utilizar serviços especializados |
| R06 — Obtenção de privilégios | Alto | Reduzir | As funções administrativas são necessárias, mas devem possuir autorização rigorosa |

### 9.3 Mapeamento dos riscos para as funções do NIST CSF

| Risco | Govern | Identify | Protect | Detect | Respond | Recover |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| R01 — Uso indevido da conta | X | X | X | X | X | X |
| R02 — Alteração indevida de dados | X | X | X | X | X | X |
| R03 — Negação de uma operação | X |  | X | X | X |  |
| R04 — Exposição de informações | X | X | X | X | X | X |
| R05 — Indisponibilidade | X | X | X | X | X | X |
| R06 — Obtenção de privilégios | X | X | X | X | X | X |

O preenchimento da tabela indica quais funções precisam ser consideradas no tratamento de cada risco. A marcação não significa que todas as funções terão a mesma importância ou a mesma quantidade de controles.

### 9.4 Plano de tratamento dos riscos

| Risco | Controles propostos | Funções relacionadas | Responsáveis | Evidências e verificação |
| --- | --- | --- | --- | --- |
| R01 — Uso indevido da conta | Autenticação multifator; nova autenticação antes de cancelamentos; encerramento seguro de sessões; notificação de operações importantes | Protect, Detect, Respond e Recover | Equipe de desenvolvimento e equipe de infraestrutura | Testes de autenticação; registros de acesso; simulação de conta comprometida; confirmação do envio de alertas |
| R02 — Alteração indevida de dados | Validação no servidor; controle de integridade; autorização para alterações; registro de valores anteriores e posteriores | Protect, Detect, Respond e Recover | Equipe de desenvolvimento e responsáveis acadêmicos | Testes de autorização; revisão dos logs; tentativa controlada de alteração indevida; restauração de dados |
| R03 — Negação de uma operação | Logs com usuário, data, horário, origem e operação; proteção contra alteração dos registros; sincronização de horário | Govern, Protect e Detect | Equipe de infraestrutura e gestão do sistema | Consulta aos logs; teste de rastreabilidade; verificação da integridade e retenção dos registros |
| R04 — Exposição de informações | Controle de acesso no servidor; menor privilégio; minimização dos dados exibidos; criptografia; monitoramento de consultas anormais | Protect, Detect, Respond e Recover | Equipe de desenvolvimento, infraestrutura e responsável pelos dados | Testes de autorização; revisão dos perfis; análise de logs; simulação de acesso a registros de terceiros |
| R05 — Indisponibilidade | Limitação de requisições; monitoramento de capacidade; escalabilidade; proteção contra tráfego malicioso; plano de contingência e canal de comunicação | Govern, Identify, Protect, Detect, Respond e Recover | Infraestrutura, gestão institucional e área acadêmica | Teste de carga; alertas de disponibilidade; simulação de incidente; teste do plano de contingência |
| R06 — Obtenção de privilégios | Autorização em todas as funções administrativas; menor privilégio; revisão periódica das permissões; autenticação reforçada para administradores | Govern, Identify, Protect e Detect | Equipe de desenvolvimento, administradores e gestão | Testes de controle de acesso; revisão das permissões; tentativa controlada de acesso administrativo |

### 9.5 Ordem inicial de implementação

A ordem inicial proposta é:

1. **Reforçar a autorização das funções administrativas e acadêmicas**, reduzindo os riscos R02, R04 e R06.
2. **Proteger as contas e operações sensíveis**, reduzindo o risco R01.
3. **Criar logs confiáveis e monitoramento**, apoiando a detecção e a investigação dos riscos R01, R02, R03, R04 e R06.
4. **Preparar a disponibilidade para os períodos críticos**, reduzindo o risco R05.
5. **Criar procedimentos de resposta e recuperação**, permitindo conter incidentes e reduzir seus impactos.
6. **Revisar periodicamente os riscos e controles**, considerando mudanças no sistema e no contexto.

A ordem poderá ser modificada conforme os recursos disponíveis, as dependências técnicas e novas informações sobre os riscos.

### 9.6 Estimativa do risco residual

A tabela apresenta uma estimativa do nível esperado após a implementação e a validação dos controles.

| Risco | Nível inicial | Nível residual esperado | Condição para aceitar o residual |
| --- | --- | --- | --- |
| R01 | Crítico | Médio | Autenticação reforçada, alertas e possibilidade de reversão funcionando |
| R02 | Alto | Baixo | Autorizações e registros de integridade validados por testes |
| R03 | Médio | Baixo | Logs protegidos, completos e disponíveis para investigação |
| R04 | Crítico | Médio | Controle de acesso, minimização e monitoramento funcionando |
| R05 | Crítico | Médio | Testes de carga, alertas e plano de contingência executados com sucesso |
| R06 | Alto | Baixo | Funções administrativas protegidas e permissões revisadas |

A redução esperada deverá ser confirmada por meio de testes e monitoramento. Caso os controles não produzam o resultado esperado, o risco deverá ser reavaliado e novos tratamentos deverão ser definidos.

### 9.7 Conclusão do tratamento

A priorização mostrou quais riscos exigem atenção inicial. O NIST CSF auxiliou na organização dos resultados esperados nas funções Govern, Identify, Protect, Detect, Respond e Recover.

O tratamento proposto combina políticas, responsabilidades, mecanismos técnicos, monitoramento e procedimentos de resposta. Isso demonstra que a segurança não depende de um único controle e não termina com a prevenção de ataques.

Os controles ainda deverão ser detalhados no projeto da arquitetura, implementados e avaliados. Somente após a obtenção de evidências será possível confirmar a redução dos riscos e decidir se o nível residual pode ser aceito.
