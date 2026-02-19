Desafio CAIXA: Desafio de Projeto DIO "Criando um APP de Organização de Finanças Pessoais com Vibe Coding" do curso "CAIXA - Inteligência Artificial na Prática da DIO":
________________________________________

Etapa 1 – Prompt Revisado e Aprimorado para o PRD (Copilot)
 
 <img width="886" height="279" alt="image" src="https://github.com/user-attachments/assets/3131a5a2-72ba-458b-b612-763dd5fa68c7" />

Contexto
Estou desenvolvendo um aplicativo de Organização de Finanças Pessoais baseado em conversas, com o objetivo de tornar o controle financeiro mais simples, natural e personalizado. O usuário interage por chat, sem necessidade de preencher formulários extensos ou usar planilhas complexas.
 
Problema
A maioria das pessoas abandona o controle financeiro porque os aplicativos tradicionais exigem muita entrada manual, pouca personalização e não se adaptam ao estilo de vida do usuário. Quero resolver essa dor oferecendo uma experiência conversacional intuitiva, acompanhada de recomendações automáticas para melhorar hábitos financeiros.
 
Público-Alvo
Pessoas que desejam começar a organizar suas finanças de forma prática, simples e acessível — especialmente usuários iniciantes ou que já tentaram outros métodos e desistiram.
 
Funcionalidades-Chave
1.	Registro de gastos e receitas via chat em linguagem natural.
2.	Classificação automática de transações.
3.	Definição e acompanhamento de metas financeiras personalizadas.
4.	Recomendações de economia e educação financeira fornecidas por um “Agente Financeiro” virtual.
5.	Relatórios simples, visuais e adaptados ao perfil do usuário.
 
Entregável da IA
Produzir um plano de MVP contendo:
•	As principais telas necessárias.
•	Os recursos essenciais para a primeira versão.
•	Um esboço de estratégia de validação inicial com usuários.
 
O conteúdo deve ser apresentado em tom educativo, com linguagem acessível, em português.

________________________________________

Etapa 2 – Plano inicial do MVP do aplicativo (Copilot)

<img width="886" height="402" alt="image" src="https://github.com/user-attachments/assets/02386012-56d9-41d1-bc89-a1e18f8e435b" />
<img width="886" height="154" alt="image" src="https://github.com/user-attachments/assets/97228c29-4618-4357-a232-4aa9e7912056" />

1) Agente Financeiro — Persona e Diretrizes de Interação

Identificação
•	Nome: Agente Financeiro (AF)
•	Papel: Consultor financeiro pessoal + analista de investimentos entry-level
•	Tom: Educativo, empático, claro, não julgador
•	Estilo de conversa: Curto → Pergunta objetiva → Sugestão prática → Opção de ação
•	Objetivo: Reduzir atrito no registro de gastos/receitas, educar sem jargões, orientar metas simples e criar hábitos consistentes

Perfil do Público (alinhado ao PRD)
•	Iniciantes ou pessoas que já tentaram planilhas/apps e desistiram
•	Querem simplicidade, rapidez e personalização mínima (sem formulários longos)

Princípios de Conversa do AF
→ “Menos passos, mais progresso” (priorizar conclusão rápida da tarefa)
→ “Primeiro entender, depois sugerir” (contexto antes de prescrever)
→ “Microvitórias” (reforço positivo a cada passo concluído)
→ “Linguagem humana” (evitar termos técnicos; quando usar, explicar)
→ “Privacidade e consentimento” (pedir autorização para conexões bancárias, relatórios, nudges)

Exemplos de mensagens do AF
•	Registro: “Anotei: R$ 27,90 no iFood como ‘Alimentação – delivery’. Quer ajustar a categoria?”
•	Dica contextual: “Você costuma pedir delivery às sextas. Quer definir um limite semanal de R$ 60?”
•	Meta: “Se guardarmos R$ 150/mês, você atinge a reserva de emergência de R$ 900 em 6 meses. Topa começar hoje?”
•	Educação: “Renda fixa é um investimento com retorno previsível. Quer ver opções seguras para começar com R$ 50?”
•	Relatórios: “Resumo da semana: gastos R$ 482 | 3 dicas de economia para você. Quer ver agora ou mais tarde?”

Limites e Segurança

•	Não dar recomendações personalizadas de investimento sem avaliação de perfil (usar suitability light via perguntas simples)
•	Explicar riscos e reforçar que não é aconselhamento profissional individualizado
•	Transparência sobre dados usados (ex.: “Uso suas categorias e hábitos para personalizar dicas”)

2) Fluxo Conceitual de Telas (Simulando Interação por Conversa)

Visão de alto nível (MVP)

→ Onboarding → Chat principal (hub) → Registro rápido → Metas → Relatórios → Dicas/Investimentos → Configurações

Fluxo detalhado

A. Onboarding (3–4 passos)
1.	Boas-vindas + Proposta de Valor
o	Mensagem: “Eu sou seu Agente Financeiro. Vamos simplificar seu controle de gastos sem planilhas.”
o	CTA: “Começar (1–2 min)”
2.	Objetivo primário
o	Pergunta: “O que você quer priorizar agora?”
o	Opções: [Controlar gastos] [Criar meta] [Entender para onde vai meu dinheiro]
3.	Preferências mínimas
o	“Quer registrar por chat, importar do banco, ou ambos?” [Chat] [Conexão Bancária] [Ambos]*
o	Conexão bancária pode ser mock ou manual no MVP, ver Plano
4.	Lembretes inteligentes (opt-in)
o	“Posso te lembrar de registrar seus gastos? Frequência sugerida: 3x/semana.” [Sim] [Não]

B. Chat Principal (hub de tarefas)
•	Input livre em linguagem natural
•	Mensagens rápidas sugeridas (chips): [Registrar gasto] [Ver resumo] [Criar meta] [Dica do dia]
•	Exemplo de sessão:
o	Usuário: “Gastei 27,90 no iFood ontem.”
o	AF: “Anotei: R$ 27,90 | Categoria: Alimentação – delivery | Data: ontem. Confirmar?” [Confirmar] [Editar]
o	Usuário: [Confirmar]
o	AF: “Quer definir um limite semanal para delivery?” [R$ 60] [Agora não]
C. Registro Rápido (atajo dentro do chat)
•	Campos inferidos pelo AF, com edição inline: valor, estabelecimento, categoria, data
•	Ações: [Salvar] [Dividir gasto] [Recorrente]

D. Metas
•	Tela/conversa:
o	AF: “Qual meta quer criar?” [Reserva emergencial] [Quitar dívida] [Viagem] [Personalizar]
o	AF: “Quanto quer juntar?” [R$ ___] “Prazo?” [mm/aaaa]
o	AF calcula contribuição mensal e propõe automação opcional
•	Dashboard de metas: progresso + % concluído + previsão de data

E. Relatórios simples
•	Resumo semanal/mensal
o	Cards: Total gasto, Top 3 categorias, Tendência vs. mês anterior, Alertas
o	Visual: gráfico de barras simples + pizza compacta
•	No chat: “Seu gasto em ‘Comida fora’ subiu 18% vs. mês passado. Quer ver dicas para reduzir?”

F. Dicas e Investimentos (educação contextual)
•	Feed curto e personalizado (máx. 3 itens)
•	Ex.: “Trocar delivery por mercado 1x/semana economiza ~R$ 80/mês”
•	Módulo de investimentos (opcional no MVP): simular cenários de renda fixa básica (CDI) com linguagem simples

G. Configurações
•	Notificações, categorias personalizadas, backup/exportação (CSV simples), privacidade

3) Plano do MVP — Funcionalidades, Recursos e Validação

3.1 Funcionalidades Principais (foco MVP)
1.	Registro por Chat (NLU leve)
→ Extrair valor, data (relativos), descrição e categoria sugerida
→ Edição rápida pelo usuário
2.	Classificação Automática
→ Regras simples + dicionário de comerciantes/categorias
→ Aprendizado incremental com confirmações do usuário
3.	Metas Financeiras
→ Configuração minimalista (valor + prazo)
→ Cálculo automático da contribuição mensal e lembretes
4.	Dicas Contextuais (Agente Financeiro)
→ Gatilhos: aumento de categoria, recorrência, desvios da meta
→ Conteúdo curto, acionável e seguro (sem jargão)
5.	Relatórios Simples e Personalizados
→ Sem sobrecarga visual; foco em 2–3 KPIs por período
→ Comparativos básicos (semana/mês anterior)

3.2 Recursos Necessários (Nível de detalhe para execução)
•	Aplicativo/Frontend:
o	Chat UI com sugestões de ação, edição inline, chips
o	Telas: Onboarding, Chat, Metas, Relatórios, Configurações
•	Linguagem Natural (NLU leve):
o	Regras + padrões (“gastei X”, “paguei Y ontem”)
o	Normalização (moeda, datas relativas)
o	Fallback para formulário compacto
•	Motor de Classificação:
o	Tabela de categorias base (Alimentação, Transporte, Moradia, Lazer, Saúde, Dívidas, Outros)
o	Mapeamento por palavras-chave/estabelecimentos
o	Correções do usuário → atualização do mapeamento
•	Regras de Dicas:
o	Triggers: variação >15% em categoria, gasto recorrente 3x+, estouro de limite, atraso de meta
o	Biblioteca de dicas educacionais curtas e auditadas
•	Metas:
o	Modelo: {nome, valor alvo, prazo, contribuição sugerida, status}
o	Cálculo automático e lembretes
•	Relatórios:
o	Agregações: por período, por categoria, top comerciantes
o	Variação % vs. período anterior
•	Dados e Infra:
o	Autenticação simples (e-mail/OTP)
o	Armazenamento seguro (criptografia em repouso)
o	Exportação CSV (backup/portabilidade)
o	Telemetria de uso (eventos de fluxo)

3.3 Plano de Validação Inicial (6 a 8 semanas)
Hipótese central: “Uma experiência conversacional reduz o atrito na entrada de dados e aumenta a consistência do controle financeiro entre iniciantes.”

Métricas de Sucesso (MVP)
•	Adoção:
o	Conversão onboarding→1º registro ≥ 70%
•	Ativação:
o	Tempo até 1ª meta criada ≤ 3 dias
•	Engajamento:
o	D+7: ≥ 35% dos usuários com ≥ 3 registros
o	D+14: ≥ 25% com relatório semanal visualizado
•	Qualitativas:
o	CSAT conversa ≥ 4,3/5
o	Clareza das dicas ≥ 4/5
•	Resultado percebido:
o	≥ 60% relatam “mais clareza para onde vai meu dinheiro” na 2ª semana

Roteiro de Experimentos
1.	Semana 1–2: Usabilidade & Mensagens
o	Teste de 1ª conversa: 10–15 usuários (entrevista + gravação de sessão)
o	Medir: entendimento da proposta, fricção de registro, tom do AF
o	Ajustar linguagem, confirmações e chips
2.	Semana 3–4: Aderência ao Hábito
o	Lembretes opt-in 3x/semana
o	Medir: taxa de registro 48h após lembrete; resposta às dicas
o	Ajustar triggers e timing
3.	Semana 5–6: Valor percebido dos Relatórios & Metas
o	Entrevista guiada + tarefa: criar 1 meta e ler 1 relatório
o	Medir: entendimento do progresso; intenção de continuar
o	Iterar visual e copy
4.	Semana 7–8: Coorte Beta Pequena (50–100 usuários)
o	Acompanhar métricas chave (adoção, ativação, engajamento)
o	Decisão: iterar MVP ou expandir funcionalidades (ex.: conexão bancária)

Instrumentação sugerida
→ Eventos: onboarding_start, onboarding_complete, first_entry_added, tip_viewed, goal_created, report_opened, reminder_sent, reminder_clicked, category_changed
→ Pesquisas in app curtas (1 pergunta) no momento certo

3.4 Escopo do MVP vs. Próximas Iterações
Incluído no MVP
•	Chat com NLU leve (regras/padrões)
•	Registro manual por texto + classificação automática inicial
•	Metas simples (valor/prazo)
•	Dicas contextuais de economia (curadoria básica)
•	Relatórios simples (semana/mês)
•	Lembretes opt-in
•	Exportação CSV
Excluído (para próximas versões)
•	Conexão bancária automática
•	OCR de notas fiscais
•	Investimentos transacionais
•	Planejamento avançado (cashflow projetado, simulações complexas)
•	Gamificação completa

3.5 Riscos e Mitigações (curto prazo)
•	Baixa precisão da classificação → Confirmação leve pelo usuário + aprendizado incremental
•	Sobrecarga de dicas → Limite de 1–3 por semana + personalização por preferência
•	Desconfiança com dados → Transparência e opt-in claro; explicar uso; exportação simples
•	Abandono após 1ª semana → Lembretes contextuais + “microvitórias” + resumos semanais enxutos
________________________________________

<img width="886" height="136" alt="image" src="https://github.com/user-attachments/assets/8ebc0a63-db9d-4049-8851-80e1eac654cb" />

O aplicativo é uma plataforma de finanças pessoais baseada em conversa, que permite ao usuário registrar gastos e receitas em linguagem natural, organizar automaticamente suas transações, acompanhar metas financeiras e receber dicas personalizadas de economia por meio de um Agente Financeiro virtual. Ele transforma o controle financeiro em uma experiência simples, intuitiva e sem planilhas, oferecendo relatórios claros e recomendações práticas para ajudar iniciantes a entender para onde vai o dinheiro e criar hábitos financeiros mais saudáveis.

________________________________________

BREVE RELATO SOBRE O PROCESSO

Usar o Copilot para criar o aplicativo foi como ter um facilitador estratégico sempre disponível.

Funcionou bem para:
•	Estruturar ideias rapidamente (organiza o PRD, define MVP, sugere métricas de sucesso);
•	Transformar objetivos vagos em fluxos acionáveis (onboarding, chat, metas, relatórios) e manter a linguagem clara e focada no público iniciante; 
•	Acelerar a geração de variantes de tom, exemplos de mensagens e critérios de validação.

Não funciona tão bem quando as instruções são ambíguas — ele pode ser convincente, porém genérico.

Aprendizados: quanto maior a riqueza de detalhes, mais contextos e restrições forem dados, melhor a qualidade das saídas. Achei útil iterar em ciclos curtos (briefing → rascunho → refinamento) e registrar padrões de conversa/estilo para ganhar consistência. Por fim, o Copilot deve ser utilizado como coautor de rascunhos e não como fonte final, validar as informações continua sendo essencial.

________________________________________
