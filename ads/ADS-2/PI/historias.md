

# 🏥 Histórias de Usuário — Sistema de Clínica Médica (Java Swing)

---

## História 1 — Login de Usuário  
**Como** usuário do sistema,  
**quero** entrar com identificação e senha,  
**para que** as funcionalidades certas sejam liberadas conforme meu perfil.  

**Critérios de Aceitação:**  
- [ ] Bloqueio após 5 tentativas falhas.  
- [ ] Perfis distintos: Atendente, Médico e Administrador.  
- [ ] Função de logout funcional.  
- [ ] Feedback em caso de credenciais inválidas.  

---

## História 2 — Gestão de Permissões  
**Como** administrador,  
**quero** atribuir perfis e permissões aos usuários,  
**para que** cada colaborador acesse apenas as funções correspondentes ao seu papel.  

**Critérios de Aceitação:**  
- [ ] Perfis com permissões por módulo (Administrativo, Agendamento, Atendimento).  
- [ ] Interface para atribuição e alteração de papéis.  
- [ ] Auditoria de mudanças em permissões.  

---

## História 3 — Gerenciamento de Funcionários  
**Como** administrador,  
**quero** cadastrar, editar e excluir funcionários,  
**para que** a base institucional permaneça atualizada e íntegra.  

**Critérios de Aceitação:**  
- [ ] Campos obrigatórios: nome, RG, CPF, endereço completo, telefones, CTPS e PIS.  
- [ ] Validação de CPF/RG/CEP.  
- [ ] Pesquisa por nome ou CPF.  

---

## História 4 — Criação de Usuários do Sistema  
**Como** administrador,  
**quero** gerar um usuário de sistema a partir de um funcionário cadastrado,  
**para que** ele possa acessar o sistema com credenciais próprias.  

**Critérios de Aceitação:**  
- [ ] Seleção de funcionário por combo.  
- [ ] Campos: iduser e password.  
- [ ] Senha com requisitos mínimos de segurança.  
- [ ] Função de reset de senha.  

---

## História 5 — Cadastro de Especialidades Médicas  
**Como** administrador,  
**quero** cadastrar especialidades médicas,  
**para que** o sistema organize corretamente os agendamentos por área médica.  

**Critérios de Aceitação:**  
- [ ] Campo “descrição” obrigatório.  
- [ ] Impedir duplicidades.  
- [ ] Listagem e busca por especialidade.  

---

## História 6 — Gerenciamento de Médicos  
**Como** administrador,  
**quero** cadastrar, editar, desativar e visualizar médicos,  
**para que** eu mantenha controle atualizado da equipe médica e garanta apenas profissionais habilitados ativos.  

**Critérios de Aceitação:**  
- [ ] Cadastro com nome, CRM e especialidade.  
- [ ] Edição de dados e inativação sem exclusão.  
- [ ] Filtro por nome, especialidade e status.  
- [ ] Bloqueio de CRM duplicado.  

---

## História 7 — Cadastro de Convênios  
**Como** administrador,  
**quero** cadastrar e gerenciar convênios,  
**para que** o sistema identifique corretamente os planos aceitos pela clínica.  

**Critérios de Aceitação:**  
- [ ] Campos: empresa, CNPJ, telefone.  
- [ ] Validação de CNPJ.  
- [ ] Flag “ativo/inativo”.  
- [ ] Convênios inativos não podem ser usados em agendamentos.  

---

## História 8 — Cadastro de Pacientes  
**Como** atendente,  
**quero** cadastrar pacientes,  
**para que** possam agendar consultas na clínica.  

**Critérios de Aceitação:**  
- [ ] Campos: nome, RG, órgão emissor, CPF, endereço completo, telefones, data de nascimento, sexo, convênio (opcional).  
- [ ] Validação de CPF e idade.  
- [ ] Busca por CPF.  
- [ ] Indicação de convênio ativo.  

---

## História 9 — Atualização de Cadastro de Paciente  
**Como** atendente,  
**quero** consultar e editar dados do paciente,  
**para que** o cadastro permaneça atualizado.  

**Critérios de Aceitação:**  
- [ ] Pesquisa por nome, CPF ou telefone.  
- [ ] Histórico de alterações.  
- [ ] Auditoria leve de edições.  

---

## História 10 — Pesquisa de Disponibilidade de Agenda  
**Como** atendente,  
**quero** visualizar horários disponíveis por médico e especialidade,  
**para que** consiga agendar consultas sem conflitos.  

**Critérios de Aceitação:**  
- [ ] Filtros por data, médico e especialidade.  
- [ ] Visualizações por dia, semana e mês.  
- [ ] Bloqueio de sobreposição de horários.  

---

## História 11 — Agendamento de Consultas  
**Como** atendente,  
**quero** agendar consultas entre pacientes e médicos disponíveis,  
**para que** o atendimento ocorra de forma organizada e sem conflitos de horários.  

**Critérios de Aceitação:**  
- [ ] Exibir apenas médicos ativos e horários livres.  
- [ ] Validação de conflito de agenda.  
- [ ] Envio de confirmação de agendamento.  
- [ ] Permitir reagendamento e cancelamento controlado.  

---

## História 12 — Registro de Retorno  
**Como** atendente,  
**quero** registrar consultas de retorno indicadas pelo médico,  
**para que** o acompanhamento do paciente seja garantido.  

**Critérios de Aceitação:**  
- [ ] Reaproveitamento do cadastro de paciente e médico.  
- [ ] Sugestão automática de janela de retorno.  
- [ ] Marcação com etiqueta “Retorno”.  

---

## História 13 — Cancelamento de Consultas  
**Como** atendente,  
**quero** cancelar consultas com motivo e senha,  
**para que** o horário volte a ficar disponível no sistema.  

**Critérios de Aceitação:**  
- [ ] Campo de motivo obrigatório.  
- [ ] Registro de quem cancelou e data.  
- [ ] Liberação imediata do horário.  
- [ ] Bloqueio para cancelamentos retroativos.  

---

## História 14 — Reagendamento de Consultas  
**Como** atendente,  
**quero** mover um agendamento existente,  
**para que** evite cancelamentos e mantenha histórico do paciente.  

**Critérios de Aceitação:**  
- [ ] Manter vínculo com paciente e médico.  
- [ ] Registro do histórico de reagendamento.  
- [ ] Verificação de conflitos de horário.  

---

## História 15 — Lista de Atendimentos do Dia  
**Como** atendente,  
**quero** visualizar a lista de consultas do dia,  
**para que** consiga organizar a recepção e o fluxo de atendimento.  

**Critérios de Aceitação:**  
- [ ] Ordenação por horário.  
- [ ] Filtro por status (agendado, confirmado, cancelado).  
- [ ] Impressão/exportação da lista.  

---

## História 16 — Acesso ao Prontuário do Paciente  
**Como** médico,  
**quero** abrir o histórico clínico do paciente,  
**para que** tenha contexto antes da consulta.  

**Critérios de Aceitação:**  
- [ ] Visualização de timeline com registros anteriores.  
- [ ] Busca por palavras-chave.  
- [ ] Restrição de acesso a médicos logados.  

---

## História 17 — Registro de Atendimento  
**Como** médico,  
**quero** registrar informações da consulta,  
**para que** o histórico do paciente fique completo.  

**Critérios de Aceitação:**  
- [ ] Campos de texto livre para queixa, diagnóstico e observações.  
- [ ] Data e hora automáticas.  
- [ ] Associação direta ao agendamento.  

---

## História 18 — Emissão de Receituário  
**Como** médico,  
**quero** gerar receituários padronizados,  
**para que** os pacientes recebam prescrições legíveis e seguras.  

**Critérios de Aceitação:**  
- [ ] Campos: medicamento, posologia e duração.  
- [ ] Exportação/Impressão em PDF.  
- [ ] Inclusão automática do CRM e assinatura do médico.  

---

## História 19 — Solicitação de Exames  
**Como** médico,  
**quero** registrar solicitações de exames,  
**para que** o acompanhamento clínico seja completo.  

**Critérios de Aceitação:**  
- [ ] Lista de exames solicitados e orientações.  
- [ ] Exportação ou impressão.  
- [ ] Marcação de pendências no prontuário.  

---

## História 20 — Anexos Clínicos  
**Como** médico,  
**quero** anexar arquivos de exames e documentos,  
**para que** o prontuário contenha todos os registros relevantes do paciente.  

**Critérios de Aceitação:**  
- [ ] Upload de arquivos (PDF, imagem).  
- [ ] Limite de tamanho configurável.  
- [ ] Visualização inline no prontuário.  
- [ ] Registro de quem anexou e quando.  

---

## História 21 — Validação e Máscaras de Campos  
**Como** usuário do sistema,  
**quero** que os campos de entrada possuam validações e máscaras,  
**para que** eu evite erros de digitação e retrabalho.  

**Critérios de Aceitação:**  
- [ ] Máscaras para CPF, CNPJ, CEP, CRM e telefone.  
- [ ] Feedback imediato em caso de erro.  
- [ ] Indicação visual de campos obrigatórios.  

---

## História 22 — Busca Global no Sistema  
**Como** usuário,  
**quero** pesquisar rapidamente por nomes, CPFs ou CRMs,  
**para que** encontre informações sem precisar navegar por várias telas.  

**Critérios de Aceitação:**  
- [ ] Atalho de teclado (Ctrl + K).  
- [ ] Resultados agrupados por categoria (Paciente, Médico, Convênio).  
- [ ] Acesso direto a registros clicáveis.  

---

## História 23 — Auditoria de Ações  
**Como** administrador,  
**quero** um log de alterações e exclusões,  
**para que** seja possível rastrear mudanças no sistema.  

**Critérios de Aceitação:**  
- [ ] Registro de quem, o que e quando alterou.  
- [ ] Exportação em CSV.  
- [ ] Histórico consultável por entidade.  

---

## História 24 — Regras de Negócio Globais  
**Como** gestor da clínica,  
**quero** garantir a consistência das operações,  
**para que** o sistema mantenha integridade e confiabilidade.  

**Critérios de Aceitação:**  
- [ ] Apenas pacientes cadastrados podem agendar.  
- [ ] Médicos inativos não aparecem na agenda.  
- [ ] Convênios inativos não podem ser usados.  
- [ ] Cancelamento exige motivo e autenticação.  
- [ ] Não permitir dois atendimentos para o mesmo médico e horário.  
