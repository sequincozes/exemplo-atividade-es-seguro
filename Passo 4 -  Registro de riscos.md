### 8.4 Registro de riscos

| ID  | Origem STRIDE          | Evento de risco                                                            | Vulnerabilidade ou condição                                                                 | Probabilidade | Impacto | Pontuação | Nível   |
| --- | ---------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------: | ------: | --------: | ------- |
| R01 | Spoofing               | Um atacante acessa a conta de um estudante e realiza operações em seu nome | Credenciais comprometidas e ausência de verificação adicional em operações importantes      |             3 |       4 |        12 | Crítico |
| R02 | Tampering              | Matrículas, vagas ou resultados são alterados indevidamente                | Validação insuficiente e proteção inadequada da integridade dos dados                       |             2 |       4 |         8 | Alto    |
| R03 | Repudiation            | Um usuário nega ter solicitado, cancelado ou alterado uma matrícula        | Logs incompletos, pouco confiáveis ou sem identificação suficiente                          |             2 |       3 |         6 | Médio   |
| R04 | Information Disclosure | Dados pessoais ou acadêmicos são acessados por pessoas não autorizadas     | Falhas de autorização e validação inadequada do usuário que solicita o registro             |             3 |       4 |        12 | Crítico |
| R05 | Denial of Service      | O sistema fica indisponível durante o período de matrículas                | Ausência de limitação de requisições e capacidade insuficiente nos períodos de maior acesso |             4 |       4 |        16 | Crítico |
| R06 | Elevation of Privilege | Um estudante obtém funções de secretaria ou administrador                  | Controle de autorização insuficiente nas funcionalidades administrativas                    |             2 |       4 |         8 | Alto    |

### 8.5 Justificativas

#### R01 — Uso indevido da conta de um estudante

A probabilidade foi classificada como média-alta porque o comprometimento de credenciais é uma situação plausível, especialmente quando usuários reutilizam senhas ou são vítimas de fraude.

O impacto foi classificado como muito alto porque o atacante pode cancelar matrículas, causar perda de vagas e gerar prejuízo acadêmico direto.

#### R02 — Alteração indevida de dados acadêmicos

A probabilidade foi classificada como média-baixa porque a alteração depende de uma falha específica de validação ou autorização.

O impacto foi classificado como muito alto porque mudanças em vagas, resultados ou matrículas podem comprometer a integridade do processo acadêmico.

#### R03 — Negação de uma operação realizada

A probabilidade foi classificada como média-baixa porque o problema depende da ausência ou insuficiência dos registros.

O impacto foi classificado como alto porque a universidade pode ter dificuldade para investigar contestações e responsabilizar o autor de uma operação.

#### R04 — Exposição de informações acadêmicas

A probabilidade foi classificada como média-alta porque falhas de autorização podem permitir consultas indevidas por usuários autenticados.

O impacto foi classificado como muito alto devido à exposição de dados pessoais e acadêmicos.

#### R05 — Indisponibilidade no período de matrículas

A probabilidade foi classificada como alta porque o aumento de acessos é previsível durante determinados períodos e também pode ser explorado por atacantes.

O impacto foi classificado como muito alto porque a indisponibilidade pode afetar muitos estudantes e impedir solicitações dentro do prazo.

#### R06 — Obtenção de permissões administrativas

A probabilidade foi classificada como média-baixa porque depende de uma falha específica no controle de autorização.

O impacto foi classificado como muito alto porque o usuário poderia alterar vagas, ofertas, permissões e matrículas.
