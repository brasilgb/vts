# Manual do Usuário - VetorOS

**Manual do Cliente**

## Plataforma de gestão operacional para atendimento técnico, financeiro e relacionamento com clientes

Este manual foi organizado para orientar o uso prático do VetorOS no dia a dia da assistência técnica. O conteúdo cobre os módulos principais, o que cada botão faz, o que o sistema executa em segundo plano e como funcionam os fluxos de e-mail, acompanhamento, garantia, avaliações e cobranças.

> **Versão do manual:** 2.2
> **Atualizado em:** 23 de julho de 2026
> **Formato:** HTML navegável

> A recomendação prática é usar esta página HTML como manual principal. Ela possui links internos, funciona bem no navegador, pode ser atualizada com facilidade e consultada pela equipe durante a rotina de atendimento.

> Atualizações recentes para usuários SaaS: perfil com imagem, troca de senha pelo menu Perfil, regras de visibilidade entre perfis, liberação de Técnico master para visualizar todas as ordens, central de aplicativos auxiliares com APKs Android, app técnico para atendimento em campo, notificações de agendamento, mensagens amigáveis em falhas de operação e confirmação visual após pagamento de assinatura. O fluxo fiscal foi simplificado para registrar manualmente NF-e nas vendas e NFS-e nas ordens, sem contratação obrigatória de API dentro do VetorOS.

> Novidades operacionais desta versão: painel com prioridades do dia, filtros rápidos de ordens, tempo no status, conferência orientativa na entrada do equipamento, aviso de possível OS duplicada, alerta de estoque baixo, ações secundárias agrupadas e linha do tempo recolhível. As telas respeitam os temas claro e escuro configurados pelo usuário.

## Sumário

1. [Introdução](#1-introdução)
2. [Visão geral do sistema](#2-visão-geral-do-sistema)
3. [Configuração inicial](#3-configuração-inicial-recomendada)
4. [Dashboard](#4-dashboard)
5. [Gestão de clientes](#5-gestão-de-clientes)
6. [Ordens de serviço](#6-ordens-de-serviço)
7. [Pagamentos de ordens](#7-pagamentos-de-ordens-de-serviço)
8. [Orçamentos](#8-orçamentos)
9. [Agendamentos](#9-agendamentos-de-visitas)
10. [Área do cliente](#10-área-do-cliente)
11. [Acompanhamentos](#11-acompanhamentos)
12. [Garantia, avaliações e qualidade](#12-garantia-avaliações-e-qualidade)
13. [Mensagens internas e WhatsApp](#13-mensagens-internas-da-equipe-e-whatsapp)
14. [Peças, produtos e estoque](#14-peças-produtos-e-estoque)
15. [Vendas](#15-vendas)
16. [Despesas](#16-despesas)
17. [Caixa diário](#17-caixa-diário)
18. [Relatórios](#18-relatórios)
19. [Configurações gerais](#19-configurações-gerais)
20. [Gestão de usuários](#20-gestão-de-usuários)
21. [Aplicativos auxiliares](#21-aplicativos-auxiliares)
22. [Upload de imagens](#22-upload-de-imagens)
23. [Importação de clientes por CSV](#23-importação-de-clientes-por-csv)
24. [Emissão fiscal](#24-emissão-fiscal)
25. [Guia rápido dos botões](#25-guia-rápido-dos-botões-mais-comuns)
26. [Boas práticas](#26-boas-práticas-de-uso)
27. [Suporte](#27-suporte)

---

## 1. Introdução

O VetorOS foi desenvolvido para empresas que trabalham com assistência técnica, manutenção, eletrônica, informática, oficinas e atendimentos externos. O sistema reúne em um único ambiente os processos de atendimento, controle operacional, fluxo financeiro e comunicação com clientes e equipe.

Ele também foi pensado para assistências que estão começando e precisam organizar a rotina com uma solução simples, produtiva e que caiba no orçamento.

A plataforma possui interface responsiva e pode ser utilizada em computadores, tablets e celulares. A proposta deste manual é mostrar o que cada área faz, quando usar cada recurso, quais ações alteram dados operacionais e quais rotinas automáticas podem ser disparadas em segundo plano.

Quando a assinatura estiver bloqueada e o pagamento for realizado pelo fluxo disponível no sistema, o acesso é liberado e uma mensagem de agradecimento confirma que a conta foi regularizada. A cobrança Pix gerada pelo provedor de pagamento usa um e-mail técnico interno para evitar envio duplicado de cobrança ao cliente, já que a fatura principal é enviada pelo VetorOS.

## 2. Visão Geral Do Sistema

**Operação**
Dashboard, clientes, ordens, orçamentos, agendamentos, mensagens internas, acompanhamentos e atendimento online.

**Financeiro**
Pagamentos de ordens, vendas, despesas, caixa diário, relatórios financeiros e emissão fiscal opcional.

**Cadastro e controle**
Peças, produtos, estoque, equipamentos, checklists, usuários e permissões.

**Comunicação**
WhatsApp, e-mails automáticos por status, lembretes de cobrança, notificações do app técnico e teste SMTP.

**Aplicativos auxiliares**
Downloads dos apps Android Vetor Imagem, Vetor Atendimento e Vetor Técnico para apoiar rotinas fora da tela principal.

## 3. Configuração Inicial Recomendada

### 3.1 Dados da empresa

Cadastre nome, telefone, endereço, e-mail e dados institucionais. Essas informações são usadas em recibos, comprovantes, impressões e comunicações.

### 3.2 Tipos de equipamento

Cadastre os tipos atendidos, como celular, notebook, impressora, televisão, tablet e outros equipamentos.

### 3.3 Checklists

Cadastre checklists por tipo de equipamento para padronizar a conferência de entrada e saída.

### 3.4 Mensagens padrão

Configure mensagens de WhatsApp para os cenários usados pela empresa, como orçamento, atualização de status e retirada.

### 3.5 Impressões e etiquetas

Ajuste os textos usados em recibos, comprovantes e etiquetas para manter o padrão visual da operação.

### 3.6 Módulos opcionais

Em **Configurações → Sistema e módulos**, é possível habilitar ou desabilitar recursos como orçamentos, peças/estoque, vendas e partes do menu operacional conforme a necessidade da empresa.

### 3.7 Configuração de e-mail

Para usar e-mails automáticos, configure SMTP com host, porta, usuário, senha, criptografia, endereço remetente e nome do remetente. O sistema também possui envio de e-mail de teste para validação.

Quando o SMTP está configurado corretamente, o sistema pode enviar e-mails de criação de ordem, atualização de status, acompanhamento de orçamento e cobrança pendente.

### 3.8 Documentos fiscais

O VetorOS mantém o controle fiscal de forma manual. Emita a NF-e ou NFS-e no sistema oficial ou serviço escolhido pela empresa e depois registre no VetorOS o número, a chave, a data, os links dos arquivos e as observações. Não é necessário contratar uma API fiscal para usar esse registro.

### 3.9 Abas de configurações

A página **Sistema e módulos** está dividida em três abas. Em **Sistema e SMTP** ficam os habilitadores gerais e os dados do servidor de e-mail. Em **Fiscal** ficam os habilitadores para registro manual de NF-e e NFS-e. Em **Operacionais** ficam metas, indicadores, visibilidade de menus e regras de acompanhamento.

### 3.10 Ordem de implantação sugerida

1. Configurar dados da empresa e validar os textos de recibo.
2. Configurar SMTP e usar o botão de teste de e-mail.
3. Definir tipos de equipamento, checklists e mensagens padrão.
4. Decidir quais módulos ficarão ativos: peças, vendas, acompanhamentos e qualidade.
5. Definir com a contabilidade onde a empresa emitirá suas notas e registrar os documentos no VetorOS.
6. Baixar e instalar os aplicativos auxiliares usados pela operação, quando houver equipe móvel.
7. Revisar metas, prazo de avaliação e intervalo de acompanhamento automático.

### 3.11 App técnico e atendimento em campo

Quando a empresa usa atendimento externo, configure os usuários técnicos, confira se o técnico está ativo e cadastre agendamentos vinculados a uma ordem de serviço. Para que a agenda apareça no app técnico, o agendamento precisa estar marcado para envio ao técnico.

O app técnico usa o mesmo login do sistema e mostra somente os atendimentos permitidos para o usuário autenticado. Técnicos comuns veem a própria agenda; técnicos com liberação master podem ter visibilidade ampliada conforme a configuração da empresa.

### 3.12 Tema da interface

O seletor de aparência permite usar o tema **Claro**, **Escuro** ou **Sistema**. No modo Sistema, o VetorOS acompanha a preferência do dispositivo. A escolha é mantida durante a navegação e também se aplica aos cartões, alertas, filtros e indicadores do painel.

## 4. Dashboard

O dashboard reúne indicadores operacionais e financeiros com gráficos, métricas e atalhos rápidos. Quando o módulo de vendas está ativo, o sistema também destaca informações comerciais e acesso rápido ao fluxo de vendas.

**Visão operacional**
Exibe ordens em andamento, status mais usados e alertas de pendências do atendimento.

**Visão financeira**
Consolida valores de ordens, vendas, despesas e indicadores do caixa.

**Alertas de qualidade**
Pode sinalizar aumento de retorno em garantia e avaliações críticas de clientes.

**Atalhos rápidos**
Facilita o acesso aos módulos mais usados da rotina diária.

O dashboard também pode mostrar indicadores de acompanhamento, fila de retorno em garantia, recuperação de avaliações críticas e métricas comerciais conforme os módulos habilitados.

### 4.1 Prioridades de hoje

A faixa **Prioridades de hoje** concentra somente situações que podem exigir uma ação da equipe. Cada item é clicável e abre a listagem já filtrada.

- **Prazo vencido:** OS abertas com previsão de entrega anterior ao dia atual.
- **Aguardando aprovação:** orçamentos enviados que ainda estão no status de orçamento gerado.
- **Aguardando retirada:** serviços concluídos em que o cliente já foi avisado.
- **Sem técnico:** ordens ativas ainda sem responsável definido.
- **Estoque baixo:** peças ou produtos cuja quantidade chegou ao estoque mínimo configurado.

O vermelho é reservado para prazos efetivamente vencidos. Os demais itens usam cores neutras para facilitar a leitura sem transformar o painel em uma tela de alertas.

### 4.2 O que analisar todos os dias

- **Ordens em atraso:** ajudam a priorizar atendimento, peças pendentes e retorno ao cliente.
- **Saldos pendentes:** mostram onde há cobrança em aberto e necessidade de contato.
- **Indicadores de garantia:** sinalizam risco de retrabalho técnico.
- **Avaliações críticas:** apontam clientes que podem exigir tratativa rápida.

### 4.3 Quem usa esta tela

- **Administrador:** acompanha resultado geral da operação, qualidade e financeiro.
- **Atendente:** usa os atalhos para abrir OS, consultar clientes e localizar pendências.
- **Gestor:** identifica gargalos, acompanha metas e decide prioridades do dia.

### 4.4 Dashboard de vendas

Quando o módulo de vendas está ativo, o dashboard financeiro apresenta leituras próprias para o comercial. O gráfico **Meios de pagamento** mostra a distribuição das vendas por Pix, cartão, dinheiro, transferência, boleto e outros meios no período selecionado.

O gráfico **Faturamento de vendas** compara vendas concluídas e despesas do mês corrente, usando linhas para facilitar a leitura da evolução diária. A tela também pode exibir resultado do período, saldo pendente em vendas, vendas canceladas e produtos mais vendidos.

Nos indicadores financeiros operacionais, os valores de faturamento, serviços e peças são apresentados com formatação monetária em reais. Isso facilita a conferência visual dos KPIs e evita leitura ambígua de valores sem o prefixo **R$**.

## 5. Gestão De Clientes

O cadastro de clientes permite registrar e consultar os dados necessários para atendimento, faturamento e relacionamento.

- Cadastrar, editar e excluir clientes.
- Pesquisar por nome ou documento.
- Consultar ordens e agendamentos vinculados.
- Visualizar total de ordens, total pago e saldo pendente por cliente.
- Enviar mensagem via WhatsApp.

### 5.1 Fluxo recomendado

1. Cadastrar o cliente com nome, telefone e formas principais de contato.
2. Revisar documento, endereço e observações antes de salvar.
3. Usar a ficha do cliente como ponto de consulta de ordens e pendências.

### 5.2 Botões e ações comuns

- **Novo cliente:** abre o formulário de cadastro.
- **Editar:** atualiza dados cadastrais e observações.
- **Excluir:** remove o cadastro quando não houver vínculo impeditivo.
- **WhatsApp:** abre o fluxo de contato rápido com o cliente.
- **Pesquisar:** filtra por nome, documento ou informação relevante.

O saldo pendente do cliente considera ordens entregues ao cliente que ainda possuem valor em aberto. Ordens em orçamento, reparo ou etapas anteriores não devem gerar cobrança pendente na ficha do cliente.

### 5.3 O que acontece ao clicar nos botões

- **Salvar cliente:** grava os dados e deixa o cadastro disponível para OS, agendamentos, vendas e consultas futuras.
- **Editar:** altera informações que passam a valer em novos atendimentos e consultas posteriores.
- **Excluir:** só deve ser usado quando o cadastro foi criado por engano e não há histórico importante vinculado.
- **WhatsApp:** ajuda a iniciar contato já com o telefone do cliente preenchido.

### 5.4 Quem pode usar cada ação

- **Administrador:** normalmente pode cadastrar, editar e excluir.
- **Atendente:** costuma cadastrar, editar e consultar.
- **Técnico:** em geral consulta dados, mas a permissão depende da configuração da empresa.

### 5.5 Importação em lote

Quando a empresa já possui uma base anterior, a importação por CSV ajuda a acelerar a implantação e reduzir retrabalho de cadastro manual.

### 5.6 App Autoatendimento

O app de autoatendimento foi pensado para ações rápidas fora da tela principal do sistema, como cadastrar clientes e consultar orçamentos. Ele usa o mesmo ambiente do VetorOS e ajuda a equipe de recepção a reduzir tempo em tarefas simples da rotina.

## 6. Ordens De Serviço

A ordem de serviço é o núcleo operacional do sistema. Nela ficam registrados os dados do cliente, equipamento, defeito, diagnóstico, valores, peças aplicadas, datas e andamento do atendimento.

- Criação, edição e exclusão de ordens.
- Vinculação de técnico responsável.
- Registro de peças, serviços executados e observações.
- Geração de recibos, checklist e documentos relacionados.
- Envio de mensagens ao cliente por WhatsApp.
- Vínculo com imagens do equipamento.
- Histórico automático de alteração de status.

Ao salvar uma OS, o sistema registra dados do cliente, equipamento e serviço. Dependendo do momento do fluxo, ele também pode gerar histórico de status, registrar logs operacionais e disparar comunicações ao cliente.

Por padrão, usuários com perfil de técnico visualizam apenas as ordens atribuídas a eles. Quando a empresa precisar que um técnico acompanhe toda a operação técnica, o administrador pode habilitar a opção **Técnico master** no cadastro do usuário. Com essa opção ativa, o técnico passa a visualizar todas as ordens de serviço da empresa.

### Status da ordem

| Código | Status | Uso prático |
| --- | --- | --- |
| 1 | Ordem aberta | Entrada inicial do equipamento e abertura do atendimento. |
| 2 | Ordem cancelada | Quando o atendimento é encerrado sem continuidade. |
| 3 | Orçamento gerado | Quando o valor foi calculado e apresentado ao cliente. |
| 4 | Orçamento aprovado | Quando o cliente autoriza a continuidade do serviço. |
| 5 | Orçamento reprovado | Quando o cliente não aprova a execução. |
| 6 | Reparo em andamento | Execução técnica em curso. |
| 7 | Serviço concluído | Reparo finalizado internamente. |
| 8 | Serviço não executado | Quando a ordem é encerrada sem realização do serviço. |
| 9 | Cliente avisado / aguardando retirada | Equipamento pronto, aguardando retirada. |
| 10 | Entregue ao cliente | Encerramento do atendimento com entrega final. |

Se o SMTP estiver configurado e o cliente tiver e-mail válido, o sistema pode enviar e-mail automático na criação da ordem e sempre que houver atualização de status.

Ao entregar uma OS, informe a quantidade de dias de garantia. Essa OS passa a ser a **origem da garantia**; ela não é um retorno. Se o mesmo equipamento voltar com um problema coberto, abra uma nova OS, marque **Esta OS é um retorno em garantia** e selecione a OS entregue anteriormente.

### 6.1 O que os principais botões fazem

- **Salvar:** grava alterações da OS, valida campos e pode registrar mudança de status.
- **Excluir:** remove a OS quando permitido pela regra do sistema.
- **Adicionar pagamento:** abre o registro financeiro da ordem.
- **Enviar acompanhamento:** dispara contato manual de orçamento.
- **Enviar lembrete de cobrança:** registra e envia uma cobrança manual ao cliente.
- **Registrar fiscal:** salva dados do comprovante ou documento fiscal vinculado à OS.
- **Imprimir recibo:** abre a versão de impressão do comprovante da ordem.
- **Visualizar detalhes:** exibe histórico, pagamentos e dados operacionais.
- **Mais ações:** reúne acompanhamento público, recibo, imagens, cobrança de orçamento, emissão fiscal e exclusão, conforme as permissões do usuário.

### 6.2 O que acontece por trás

- O sistema grava histórico de status para rastreabilidade da OS.
- Logs operacionais ajudam a identificar ações importantes como envio de acompanhamento, cobrança e confirmações do cliente.
- Uma OS só é registrada como retorno quando a equipe marca essa opção e seleciona a OS de origem.
- O sistema permite selecionar apenas uma OS entregue, do mesmo cliente e equipamento, com garantia ativa.
- Quando o cliente interage no portal público, a OS também recebe atualização e registro de log.

### 6.3 Quando o status muda, o sistema pode fazer isto

- **Ordem aberta:** inicia o histórico da OS e pode permitir comunicação inicial com o cliente.
- **Orçamento gerado:** deixa a ordem elegível para aprovação pública e para acompanhamento comercial.
- **Orçamento aprovado:** libera a continuidade do serviço e ajuda a medir conversão.
- **Serviço concluído:** prepara o fluxo de aviso ao cliente e retirada.
- **Cliente avisado / aguardando retirada:** pode acionar lembretes e registros de confirmação.
- **Entregue ao cliente:** encerra a OS e pode iniciar o prazo para avaliação e garantia.

### 6.4 Quem costuma usar cada ação da OS

- **Administrador:** acesso total, inclusive exclusão, financeiro e fiscal.
- **Atendente:** abertura da OS, atualização de status, contato com cliente e pagamentos.
- **Técnico:** diagnóstico, observações técnicas, peças utilizadas e andamento do reparo.

### 6.5 Fluxo recomendado da OS

1. Abrir a ordem com o máximo de detalhes do equipamento e do defeito.
2. Registrar acessórios, senha, observações e estado do item.
3. Atualizar o status sempre que a etapa operacional mudar.
4. Gerar orçamento e enviar ao cliente quando necessário.
5. Registrar conclusão, aviso ao cliente, retirada e entrega final.

### 6.6 Documentação do atendimento

Use imagens, checklist, observações e histórico de status para manter rastreabilidade do atendimento e reduzir dúvidas futuras.

### 6.7 Fluxo de garantia e retorno

1. Na OS do serviço original, informe os dias de garantia.
2. Marque a OS como entregue ao cliente. O vencimento da garantia será calculado a partir da entrega.
3. Se o equipamento voltar dentro do prazo por um problema coberto, crie uma nova OS.
4. Na nova OS, marque **Esta OS é um retorno em garantia**.
5. Selecione a OS original no campo **OS de origem** e salve.

> Não marque a OS original como retorno. A primeira OS origina a garantia; somente a nova OS, aberta quando o equipamento volta, deve ser identificada como retorno em garantia. Depois de registrada, a nova OS permanece marcada para preservar o histórico, mesmo após o vencimento da garantia original. Após salvar, o vínculo não pode ser desmarcado ou trocado na edição, garantindo a integridade dos indicadores e do histórico operacional.

Na listagem de ordens, a situação aparece ao lado do status como **Garantia até** ou **Garantia encerrada em**. Use o filtro **Garantia ativa** para mostrar somente as OS que ainda estão dentro do prazo. O filtro **Retorno em garantia** continua separado e mostra as novas OS vinculadas a uma garantia anterior.

### 6.8 Conferência de entrada

Ao abrir uma nova OS, a faixa **Conferência de entrada** acompanha o preenchimento de cliente, equipamento, marca e modelo, defeito relatado, conservação, acessórios e previsão. O contador é orientativo: ele ajuda a evitar esquecimentos, mas não torna obrigatórios campos que a empresa decidiu manter como opcionais.

1. Selecione o cliente e o tipo de equipamento.
2. Informe marca, modelo e o defeito relatado com as palavras do cliente.
3. Registre o estado de conservação e os acessórios recebidos.
4. Defina a previsão e confira o contador antes de salvar.
5. Use imagens quando houver avarias, trincas ou outros detalhes que precisem de evidência.

### 6.9 Aviso de possível duplicidade

Quando já existe uma OS ativa para o mesmo cliente e equipamento, o formulário mostra um aviso com links para consultar as ordens encontradas. O aviso não bloqueia o cadastro, porque um mesmo equipamento pode ter atendimentos simultâneos legítimos, mas a equipe deve conferir antes de criar outra OS.

### 6.10 Busca, filtros e tempo no status

A busca da listagem aceita número da OS, cliente, documento, telefone, WhatsApp, equipamento e modelo. Além dos status normais, estão disponíveis filtros para **Prazo vencido**, **Sem técnico**, **Aguardando retirada**, feedback, orçamento parado, cobrança pendente, garantia e financeiro em aberto.

Ao lado do status, o sistema informa há quantos dias a ordem permanece naquela etapa. Passe o cursor sobre a informação para consultar a data e hora da última mudança. Esse indicador ajuda a encontrar gargalos, mas não altera automaticamente o status da OS.

### 6.11 Linha do tempo

A linha do tempo reúne mudanças de status, pagamentos, peças, imagens, documentos fiscais, comunicações e outras ações registradas. Para manter a tela limpa, são mostrados inicialmente os eventos mais recentes. Use **Ver histórico completo** para expandir e **Mostrar somente os recentes** para recolher novamente.

## 7. Pagamentos De Ordens De Serviço

O VetorOS permite controlar o financeiro de cada ordem separadamente, com pagamentos totais ou parciais. Esse fluxo foi adicionado ao manual porque é uma das rotinas mais importantes da operação.

**Resumo financeiro exibido**
Valor de peças, valor de serviço, total da ordem, total pago e saldo restante.

**Formas de pagamento**
Pix, cartão, dinheiro, transferência e boleto.

**Regras do lançamento**
O valor informado não pode ser maior que o saldo restante da ordem.

**Dependência operacional**
O caixa diário deve estar aberto para registrar pagamentos.

Quando o financeiro de OS está ativo, a ordem já foi entregue ao cliente, ainda há saldo pendente e o e-mail do cliente está válido, o sistema pode enviar lembrete de cobrança por e-mail.

Depois de emitir uma NFS-e fora do VetorOS, registre manualmente seus dados na ordem para manter o histórico fiscal junto do atendimento.

### 7.1 Botões e comportamentos

- **Registrar pagamento:** grava valor, data, forma de pagamento e observações.
- **Excluir pagamento:** remove o lançamento quando a regra do caixa permitir.
- **Dados de pagamento:** mostra histórico e total pago.
- **Lembrete de cobrança:** envia contato manual ao cliente e registra a ação quando o financeiro de OS estiver ativo.

Nos bastidores, o sistema impede pagamento maior que o saldo, exige caixa aberto para lançamento e atualiza o total pago da ordem para cálculo de saldo restante.

### 7.2 Quando registrar ou excluir

- **Registrar pagamento:** use no momento exato do recebimento para manter caixa e relatórios corretos.
- **Excluir pagamento:** use apenas quando houve erro de lançamento, recebimento duplicado ou necessidade de correção autorizada.
- **Lembrete de cobrança:** use quando a ordem já foi entregue ou está pronta e ainda existe saldo em aberto.

### 7.3 Quem pode usar

- **Administrador:** normalmente pode registrar e excluir pagamentos.
- **Atendente/financeiro:** costuma registrar recebimentos e enviar cobrança.
- **Técnico:** geralmente apenas consulta, salvo regra interna diferente.

### 7.4 Boas práticas no recebimento

1. Conferir o saldo antes de lançar o pagamento.
2. Selecionar a forma de pagamento correta.
3. Evitar deixar recebimentos para registrar depois, para não distorcer caixa e relatórios.

## 8. Orçamentos

O módulo de orçamentos permite criar, editar, excluir e imprimir propostas. Em muitas operações, ele é parte do fluxo da ordem de serviço e pode anteceder a aprovação do cliente.

Quando o orçamento é gerado dentro da OS, o cliente pode aprovar ou reprovar pela área pública, desde que o link da ordem tenha sido compartilhado.

- **Gerar orçamento:** registra descrição e valor proposto.
- **Enviar acompanhamento de orçamento:** cobra resposta do cliente e registra o contato.
- **Aprovação pública:** altera o status da OS quando o cliente responde pelo portal.

### 8.1 Quando o cliente responde

- **Se aprovar:** a ordem segue para continuidade técnica e entra na medição de conversão.
- **Se reprovar:** a decisão fica registrada e a equipe pode encerrar ou redirecionar a tratativa.
- **Se não responder:** a ordem pode entrar na fila de acompanhamentos, conforme a configuração operacional.

### 8.2 Quem usa cada ação

- **Administrador e atendente:** geram orçamento, enviam acompanhamento e fazem tratativa comercial.
- **Cliente final:** aprova ou reprova pelo link público quando o recurso estiver disponível.

### 8.3 Campos de seleção

No formulário de orçamento, campos como cliente, equipamento, garantia, marca e modelo usam seleção pesquisável. Digite parte do nome ou do modelo para localizar opções cadastradas sem precisar percorrer listas longas.

Usuários com permissão para gerenciar equipamentos também encontram o botão **+** ao lado do campo Equipamento. Ele abre o mesmo cadastro rápido usado nas ordens de serviço. Ao salvar um novo tipo, o equipamento é incluído na lista e selecionado no orçamento.

### 8.4 Consulta de orçamentos no app autoatendimento

Quando a empresa usa o app de autoatendimento, a equipe pode consultar informações de orçamento pelo celular. Esse recurso ajuda em atendimentos rápidos, principalmente quando o colaborador precisa localizar uma referência sem abrir a tela completa do sistema web.

## 9. Agendamentos De Visitas

- Cadastrar, editar e excluir agendamentos.
- Vincular cliente e técnico.
- Acompanhar status do agendamento.
- Enviar mensagem ao técnico por WhatsApp.
- Enviar o atendimento para o app técnico quando a empresa usa equipe em campo.

Os status usuais do agendamento são aberto, em atendimento e fechado.

Esse módulo é útil para assistência externa, coleta, entrega técnica e visitas programadas.

A listagem, o cadastro e a edição exibem uma breve descrição no topo para indicar o objetivo de cada tela. Use a busca e os filtros para localizar rapidamente atendimentos da equipe.

No cadastro e edição, cliente, técnico responsável e status usam campos de seleção. Técnico e status são obrigatórios; se algum deles ficar em branco, o sistema exibe a validação antes de salvar. A data e hora podem ser escolhidas em um componente de calendário e horário para agilizar o preenchimento.

### 9.1 O que os botões normalmente fazem

- **Novo agendamento:** reserva a visita e organiza a agenda operacional.
- **Editar:** corrige data, técnico, observações ou endereço.
- **Excluir:** remove o compromisso quando ele não será mais realizado.
- **WhatsApp do técnico:** acelera a comunicação da equipe em campo.

### 9.2 Envio para o app técnico

Ao marcar um agendamento para envio ao técnico, ele passa a ficar disponível no app técnico do usuário responsável. O app mostra a agenda pendente, dados do cliente, endereço, telefone, WhatsApp, dados da ordem, equipamento, defeito informado e observações relevantes para o atendimento.

O app técnico respeita o usuário logado. Isso significa que cada técnico visualiza apenas os atendimentos atribuídos a ele, salvo quando a empresa liberar visibilidade ampliada para o perfil técnico.

### 9.3 Fluxo recomendado no app técnico

1. O atendente cria ou edita o agendamento no sistema e marca o envio ao técnico.
2. O técnico abre o app, confere os atendimentos pendentes e acessa os detalhes da visita.
3. Ao chegar no local, registra o **check-in**. Quando permitido pelo aparelho, o app também registra a localização.
4. Durante o atendimento, preenche checklist, diagnóstico, solução e observações técnicas.
5. Se necessário, anexa imagens da ordem para documentar o serviço.
6. Quando houver recebimento no local, registra o pagamento com valor, forma e observação.
7. Ao finalizar, registra o **check-out**. O sistema exige check-in antes do encerramento e pode exigir relatório/checklist salvo antes de finalizar.

### 9.4 Notificações de agendamento

Quando as notificações estiverem permitidas no aparelho, o app técnico pode avisar o usuário sobre novos atendimentos enviados. A permissão de notificação é solicitada pelo próprio sistema operacional do celular.

Se a notificação não puder ser registrada por falta de internet, permissão negada ou configuração do aparelho, o atendimento ainda pode ser consultado ao abrir o app e atualizar a agenda.

### 9.5 Trabalho sem conexão

O app técnico mantém dados recentes em cache para consulta quando a conexão estiver instável. Alterações como relatório e checklist podem ser guardadas para sincronização posterior. Mesmo assim, ações que dependem de confirmação imediata do servidor, como envio de imagem, pagamento e encerramento, devem ser conferidas quando a internet voltar.

### 9.6 Boas práticas para atendimento externo

- Enviar ao técnico apenas agendamentos confirmados e vinculados à ordem correta.
- Conferir telefone, WhatsApp e endereço do cliente antes da visita.
- Orientar a equipe a registrar check-in e check-out no momento real do atendimento.
- Salvar diagnóstico e solução antes de finalizar para manter histórico técnico completo.
- Usar imagens somente quando elas ajudam a comprovar estado, defeito ou serviço realizado.

## 10. Área Do Cliente

Cada ordem pode gerar um link de acompanhamento com token. Esse link permite que o cliente acompanhe o andamento do atendimento diretamente no navegador, sem acessar a área administrativa.

- Status atual da ordem.
- Dados do equipamento.
- Informações principais do atendimento.
- Resumo financeiro da ordem.
- Links para comprovantes, orçamento, pagamentos e nota quando disponíveis.
- Acompanhamento online com mais transparência para o cliente.

Dependendo do status da ordem, o cliente também pode executar ações no próprio painel público: aprovar ou reprovar orçamento, confirmar o recebimento do aviso de conclusão, confirmar a retirada do equipamento e deixar avaliação com nota em 5 estrelas e opinião textual.

### 10.1 Ações públicas do cliente

- **Aprovar orçamento:** move a OS para orçamento aprovado quando a etapa permitir.
- **Reprovar orçamento:** registra reprovação e encerra a proposta.
- **Confirmar aviso:** marca que o cliente recebeu o aviso de conclusão.
- **Confirmar retirada:** só libera a entrega pública se não houver saldo pendente.
- **Enviar avaliação:** grava nota e comentário do cliente.

Essas ações públicas também geram histórico, logs e podem alimentar indicadores de qualidade e recuperação de satisfação.

### 10.2 O que o sistema registra nessas ações

- **Aprovação ou reprovação:** grava a resposta do cliente e altera o andamento da ordem.
- **Confirmação de aviso:** mostra que o cliente tomou ciência de que a ordem está pronta.
- **Confirmação de retirada:** ajuda a comprovar a finalização pública do fluxo.
- **Avaliação:** entra nos indicadores de satisfação e pode gerar tratativa se a nota for baixa.

### 10.3 Quando compartilhar o link

O ideal é enviar o link logo após a abertura da ordem ou junto da primeira atualização relevante. Isso reduz consultas repetidas por telefone e melhora a percepção de transparência.

### 10.4 Chave de acesso da página pública

Em **Configurações > Sistema e módulos > Operacionais**, a empresa pode ativar **Solicitar chave de acesso**. Quando essa proteção estiver ativa, o cliente deverá informar a chave alfanumérica de 8 caracteres da OS antes de visualizar a página, orçamento, pagamentos, comprovantes ou enviar respostas.

- A chave aparece na edição da OS para consulta da equipe.
- Os e-mails automáticos que contêm o link também apresentam a chave.
- As mensagens de WhatsApp geradas pelo sistema acrescentam a chave abaixo do link.
- Após a validação, o navegador permanece autorizado durante a sessão.
- Tentativas de acesso são limitadas para reduzir adivinhação de chaves.

## 11. Acompanhamentos

O módulo de acompanhamentos organiza contatos pendentes com clientes em duas frentes: **orçamento parado** e **cobrança pendente**. Ele ajuda a equipe a não perder oportunidades nem deixar valores em aberto sem retorno.

**Acompanhamento de orçamento**
Localiza ordens com orçamento gerado e sem resposta do cliente após o prazo configurado.

**Acompanhamento de cobrança**
Localiza ordens entregues ou concluídas com saldo pendente e cliente elegível para contato.

**Tarefas da equipe**
Permite atribuir o contato a um usuário específico e acompanhar tratativas pendentes.

**Performance comercial**
Compara contatos realizados com resultados obtidos em conversão e recuperação.

### 11.1 Botões e ações

- **Pausar:** interrompe a cadência automática para aquela OS.
- **Retomar:** volta a permitir acompanhamento automático ou tarefa pendente.
- **Responder:** registra o retorno do cliente no histórico da OS.
- **Concluir tarefa:** remove a pendência operacional do responsável.
- **Adiar:** snooze da tarefa até uma nova data.
- **Atribuir:** define o usuário responsável pela ação.
- **Atribuir selecionadas:** faz atribuição em lote.

### 11.2 O que o sistema faz por trás

- Consulta ordens elegíveis com base em status, data da última atualização, entrega e saldo pendente.
- Considera orçamento parado quando a OS está em orçamento gerado e sem retorno dentro da janela configurada.
- Considera cobrança pendente somente para OS entregue ao cliente, com saldo em aberto e financeiro de OS ativo.
- Respeita o intervalo mínimo entre contatos configurado em Operacionais, mesmo para a fila manual.
- Ignora ordens pausadas, adia tarefas snoozadas e registra cada envio em log.
- Quando um contato é feito ou uma tarefa é concluída, a pendência sai da fila ativa durante a janela configurada.
- Se a pendência continuar aberta depois desse prazo, ela volta a aparecer para novo acompanhamento.
- Pode disparar e-mails automáticos quando a automação está ligada, o SMTP está válido e as regras do módulo permitem.
- Usa cron para executar acompanhamentos automáticos de orçamento e cobrança.

A tela de acompanhamentos mostra pendências ativas, não um histórico completo de todos os contatos. Para consultar o histórico, use os registros e a linha do tempo da própria ordem.

### 11.3 Quando usar cada ação

- **Pausar:** quando o cliente pediu prazo, está viajando ou já respondeu por outro canal.
- **Retomar:** quando a tratativa volta a exigir contato ativo da equipe.
- **Responder:** quando houve retorno do cliente e isso precisa ficar documentado.
- **Atribuir:** quando você quer deixar claro quem será responsável pelo próximo contato.
- **Concluir tarefa:** quando a pendência realmente terminou, para não poluir a fila.

### 11.4 Automação e janela de retorno

A opção de janela fica em **Configurações gerais > Operacionais > Intervalo de follow-up com cliente**. O link **Alterar janela**, quando exibido nos acompanhamentos, leva diretamente para essa configuração.

Se o envio automático estiver desligado, o sistema não envia e-mails automáticos, mas continua usando a janela para organizar a fila manual. O botão **Pausar automação** aparece apenas quando a automação está ativa para aquele tipo de acompanhamento.

### 11.5 Quem normalmente usa

- **Administrador:** acompanha a fila, ajusta regras e redistribui pendências.
- **Atendente/comercial:** executa os contatos e registra as respostas.
- **Gestor:** usa os dados para cobrança de rotina, conversão e recuperação.

## 12. Garantia, Avaliações E Qualidade

O módulo de qualidade reúne dois grandes objetivos: acompanhar **retorno em garantia** e monitorar **avaliações de clientes**.

### 12.1 Garantia

- O sistema calcula o vencimento usando a data de entrega e os dias de garantia informados na OS original.
- A OS original é a origem da cobertura e não deve ser marcada como retorno.
- Quando o equipamento volta dentro da cobertura, a equipe marca a nova OS como retorno e seleciona a OS de origem.
- Os relatórios e indicadores usam essa marcação para medir taxa de retorno.
- Há limiar configurável para alerta visual de excesso de garantia.

#### 12.1.1 O que a equipe deve observar

- **Entrada de nova OS dentro do prazo:** verificar se realmente é retorno coberto pela garantia.
- **Motivo recorrente:** usar o histórico para identificar falha de processo, peça ou execução.
- **Excesso de garantias:** tratar como sinal de atenção gerencial, não só como caso isolado.

#### 12.1.2 Como visualizar os retornos

Abra **Garantias e avaliações** e acesse a aba **Retornos em garantia**. A tabela **Ordens que retornaram em garantia** apresenta a OS de retorno, a OS de origem, cliente, equipamento, técnico, status e data de entrada. Use o botão **Abrir OS** para consultar ou corrigir o atendimento.

### 12.2 Avaliações

- Após a entrega, o cliente pode deixar nota e comentário no portal público.
- O sistema calcula quantidade de respostas, média de nota e taxa de resposta.
- Avaliações com nota baixa entram na fila de recuperação.

### 12.3 Recuperação de avaliações críticas

- **Atualizar tratativa:** define responsável, status e observações.
- **Status pendente:** caso ainda sem ação iniciada.
- **Status em tratativa:** caso o time já esteja atuando.
- **Status resolvido:** caso a recuperação tenha sido concluída.

Nos bastidores, o sistema registra log operacional e auditoria da atualização da tratativa. Isso é importante para histórico interno, análise gerencial e acompanhamento da equipe.

### 12.4 Quem usa esta área

- **Administrador e gestor:** acompanham indicadores, limites e recorrência de problemas.
- **Atendente:** registra tratativas de avaliação e ajuda na recuperação de clientes insatisfeitos.
- **Técnico:** consulta retornos em garantia para entender padrões de falha e melhorar a execução.

## 13. Mensagens Internas Da Equipe E WhatsApp

O módulo de mensagens internas serve para comunicação operacional entre usuários do sistema. O remetente pode editar ou excluir a mensagem, e o destinatário pode marcar como lida.

Esse recurso é indicado para alinhamentos rápidos da equipe sem misturar a comunicação interna com as mensagens enviadas ao cliente.

Na listagem, use os filtros para consultar mensagens recebidas, enviadas ou relacionadas ao seu usuário, além de separar mensagens lidas e não lidas. Administradores podem ter uma visão mais ampla conforme as permissões da conta.

### 13.1 Modelos de WhatsApp

O módulo de mensagens do WhatsApp armazena textos padrão para comunicação com clientes, como orçamento, cobrança, aviso de conclusão e pedido de feedback.

- **Salvar modelo:** atualiza o texto padrão usado pela operação.
- **Restaurar padrão:** volta para o texto sugerido pelo sistema.
- **Prévia:** mostra como a mensagem ficará com variáveis substituídas.

### 13.2 O que acontece ao usar essas telas

- **Mensagem interna:** registra comunicação entre usuários sem depender de aplicativos externos.
- **Editar mensagem:** corrige texto já enviado quando a regra da tela permitir.
- **Marcar como lida:** ajuda a equipe a saber se a orientação interna já foi vista.
- **Modelo de WhatsApp:** padroniza textos de cobrança, aviso, orçamento e pós-atendimento.
- **Campo Para:** permite escolher o destinatário da mensagem interna por seleção pesquisável.

### 13.3 Quem costuma usar

- **Atendente:** usa modelos prontos e alinhamentos internos com frequência.
- **Administrador:** padroniza mensagens e revisa o tom institucional.
- **Técnico:** consulta instruções internas quando participa do fluxo operacional.

## 14. Peças, Produtos E Estoque

O sistema permite cadastrar peças e produtos para uso em ordens e em vendas. O estoque acompanha a quantidade dos itens e é atualizado conforme movimentações operacionais.

- Cadastro, edição e exclusão de itens.
- Controle de estoque por quantidade.
- Uso de peças em ordens de serviço.
- Baixa de estoque em vendas.
- Devolução ao estoque quando uma venda é cancelada.

### 14.1 O que os botões normalmente fazem

- **Novo item:** cria a peça ou produto para uso futuro em OS e vendas.
- **Editar:** atualiza nome, custo, preço, categoria e saldo quando permitido.
- **Excluir:** remove cadastro sem utilidade ou criado por engano.
- **Aplicar na OS:** vincula a peça ao atendimento e impacta o custo e o estoque.

### 14.2 O que o sistema faz por trás

- Baixa o estoque quando a peça é consumida em OS ou venda concluída.
- Pode devolver quantidade ao estoque quando a venda é cancelada.
- Ajuda a compor valor da ordem e relatórios de produtos.

## 15. Vendas

O módulo de vendas é opcional e pode ser habilitado nas configurações. Quando ativo, o sistema permite registrar vendas de produtos com baixa automática no estoque e controle financeiro.

- Registro de venda com cliente opcional.
- Escolha da forma de pagamento.
- Registro de valor total e valor pago.
- Status financeiro: pendente, parcial, pago e cancelado.
- Cancelamento de venda com devolução dos itens ao estoque.
- Registro manual dos dados da NF-e emitida no sistema fiscal escolhido pela empresa.

O sistema exige caixa aberto para concluir uma venda e não permite valor pago acima do total.

Ao cancelar uma venda, o sistema pode devolver o item ao estoque e registrar logs de operação e auditoria.

No dashboard de vendas, os meios de pagamento são agrupados para facilitar a análise. Formas equivalentes, como cartão e cartão de crédito, aparecem juntas; meios não classificados entram como outros.

### 15.1 Botões e responsabilidades

- **Nova venda:** cria o lançamento comercial e reserva os itens até a conclusão.
- **Finalizar:** grava pagamento, baixa estoque e atualiza o caixa.
- **Cancelar:** encerra a venda e devolve os itens ao estoque quando aplicável.
- **Registrar NF-e:** salva manualmente número, chave, data, links e observações do documento emitido fora do VetorOS.

## 16. Despesas

O módulo de despesas registra saídas financeiras do dia a dia. Cada despesa possui número, data, descrição, categoria, valor e observações.

- Lançamento, edição e exclusão de despesas.
- Pesquisa por descrição, observação ou número.
- Filtro por categoria.
- Uso em conjunto com caixa e relatórios financeiros.

### 16.1 Quando lançar uma despesa

- **No mesmo dia:** para manter caixa e relatórios fiéis à operação real.
- **Com categoria correta:** para facilitar análise posterior de custos.
- **Com observação clara:** para evitar dúvida no fechamento do caixa.

### 16.2 Quem costuma usar

- **Administrador/financeiro:** registram, editam e revisam despesas.
- **Gestor:** acompanha volume, categorias e recorrência dos gastos.

## 17. Caixa Diário

O caixa diário centraliza a operação financeira do dia. Ele precisa estar aberto para registrar vendas e pagamentos de ordens.

1. Abrir o caixa com saldo inicial e observações.
2. Registrar vendas e pagamentos ao longo do expediente.
3. Registrar sangrias quando houver retirada de dinheiro do caixa aberto.
4. Informar entradas e saídas manuais no fechamento.
5. Fechar o caixa com saldo contado.
6. Conferir diferença entre saldo esperado e saldo informado.

No fechamento, o sistema consolida total de vendas concluídas, vendas canceladas, pagamentos de ordens, sangrias, entradas manuais, saídas manuais e diferença apurada.

### 17.1 O que cada etapa faz

- **Abrir caixa:** libera a operação financeira do dia.
- **Registrar recebimentos:** alimenta o saldo esperado automaticamente.
- **Registrar sangria:** documenta retirada de dinheiro durante o expediente, com valor, motivo, usuário e horário.
- **Informar saídas:** permite refletir retiradas e despesas do expediente.
- **Fechar caixa:** compara o saldo do sistema com o saldo contado.

### 17.2 Sangria de caixa

A sangria deve ser usada quando parte do dinheiro físico é retirada do caixa aberto antes do fechamento, por exemplo para envio ao cofre, depósito bancário ou redução de numerário no balcão.

- **Quando registrar:** no momento exato da retirada, enquanto o caixa ainda está aberto.
- **Dados obrigatórios:** valor da sangria e motivo da retirada.
- **Regra de saldo:** o sistema não permite sangria maior que o saldo esperado atual do caixa.
- **Impacto no caixa:** sangrias ativas reduzem o saldo esperado e entram no resumo do fechamento.
- **Histórico:** cada sangria guarda data, usuário, valor e motivo para conferência posterior.

Se uma sangria for lançada incorretamente, use a ação **Cancelar** na lista de sangrias do caixa aberto. O sistema exige o motivo do cancelamento, mantém o lançamento no histórico com identificação de quem cancelou e deixa de considerar o valor no saldo esperado. Sangrias de caixas já fechados não podem ser canceladas.

### 17.3 Fechamento e conferência

No fechamento, informe o saldo contado em dinheiro e, se necessário, entradas ou saídas manuais que não vieram de vendas, pagamentos de ordens ou sangrias. O saldo esperado considera saldo inicial, vendas concluídas, pagamentos de ordens, entradas manuais, saídas manuais e sangrias não canceladas.

- Use observações do fechamento para explicar diferença entre saldo esperado e saldo contado.
- Revise sangrias canceladas antes de fechar, pois elas permanecem visíveis no histórico.
- Após o fechamento, o caixa fica bloqueado para novas sangrias e cancelamentos.

### 17.4 Quem deve usar com mais cuidado

- **Atendente/caixa:** precisa registrar tudo no momento correto.
- **Administrador/gestor:** conferem diferenças e auditam inconsistências.

## 18. Relatórios

Os relatórios podem ser filtrados por período e ajudam no acompanhamento operacional e gerencial.

- Ordens de serviço.
- Clientes.
- Agendamentos.
- Vendas.
- Peças e produtos.
- Caixa diário, incluindo saldos, sangrias e diferenças de fechamento.
- Despesas.

Dependendo do relatório, o sistema também monta totais consolidados para impressão e exportação em PDF.

### 18.1 Indicadores de qualidade

Além dos relatórios tradicionais, o sistema possui acompanhamento de qualidade com foco em retorno em garantia e avaliações de clientes.

- Quantidade e taxa de retorno em garantia.
- Limite percentual configurável para gerar alerta visual.
- Notas médias e avaliações com nota baixa.
- Tratativa de avaliações críticas com responsável e status.

### 18.2 Acompanhamentos e tarefas

O módulo de acompanhamentos ajuda a localizar contatos pendentes com clientes em orçamento e cobrança, enquanto a área de tarefas organiza a tratativa operacional do time.

- Fila de acompanhamento de orçamento.
- Fila de acompanhamento de cobrança.
- Pausa e retomada de cadências.
- Resposta manual do cliente e encerramento da pendência.
- Atribuição de tarefas para usuários da equipe.

### 18.3 Performance comercial

A performance comercial compara os contatos realizados com a recuperação efetiva, permitindo acompanhar a conversão de orçamentos e a recuperação de cobranças ao longo do período.

### 18.4 Como usar na rotina

1. Revisar o dashboard diariamente para alertas rápidos.
2. Usar Acompanhamentos para priorizar contatos com clientes.
3. Usar Tarefas para distribuir pendências entre os responsáveis.
4. Usar Performance comercial para medir resultado real dos contatos.
5. Usar Garantia/Avaliações para identificar falhas recorrentes e clientes insatisfeitos.

### 18.5 Quem costuma consultar cada relatório

- **Administrador:** visão completa de operação, faturamento, inadimplência e qualidade.
- **Gestor:** usa principalmente performance comercial, garantia, caixa e despesas.
- **Atendente:** consulta ordens, clientes e pendências da rotina.

## 19. Configurações Gerais

O menu de configurações concentra os cadastros administrativos e o comportamento do sistema.

- Dados da empresa.
- Mensagens do WhatsApp.
- Impressões de recibos.
- Impressão de etiquetas.
- Configurações fiscais.
- Tipos de equipamento.
- Checklists.
- Aplicativos auxiliares.
- Ajustes e avaliações.
- Sistema e módulos.

Em Sistema e módulos também ficam os parâmetros de SMTP, o habilitador de módulos opcionais, o disparo do e-mail de teste e as regras operacionais do sistema.

**Sistema e SMTP**
Reúne habilitadores gerais do sistema, configurações de envio de e-mail e teste SMTP.

**Fiscal**
Habilita o registro manual de NF-e de produtos e NFS-e de serviços. A emissão acontece fora do VetorOS e o comprovante é registrado depois no sistema.

**Operacionais**
Reúne metas, indicadores, regras de avaliação, intervalo de acompanhamento e visibilidade dos menus operacionais.

**Menus operacionais**
É possível mostrar ou ocultar Acompanhamentos, Tarefas, Performance comercial e Garantia/Avaliações.

**Acompanhamento automático**
O envio automático pode ser ligado ou desligado. Se estiver desligado, o sistema não envia novos contatos automáticos de orçamento ou cobrança.

**Aplicativos auxiliares**
Centraliza o download dos APKs Android complementares e informa quando cada arquivo ainda não está disponível para instalação.

### 19.1 Visibilidade dos menus operacionais

Em Operacionais, é possível decidir se alguns menus devem aparecer ou não para a empresa. Isso ajuda a simplificar a navegação quando um recurso ainda não faz parte da rotina.

- Acompanhamentos.
- Tarefas.
- Performance comercial.
- Garantia/Avaliações.

### 19.2 Regras de acompanhamento

O intervalo de acompanhamento define quantos dias o sistema deve esperar antes de considerar um novo contato elegível. Esse intervalo organiza tanto a fila manual quanto os contatos automáticos. Se a opção de envio automático estiver desligada, o sistema não dispara acompanhamentos automáticos, mas a janela continua sendo usada para não repetir contatos cedo demais.

O ajuste fica em **Operacionais > Intervalo de follow-up com cliente**. Essa é a mesma janela mostrada na tela de acompanhamentos quando uma pendência informa que está dentro ou fora do prazo configurado.

### 19.3 Avaliações e metas

Também é possível configurar o prazo para solicitar avaliação do cliente após a entrega e definir metas mínimas para conversão de orçamento e recuperação de cobrança.

### 19.4 O que o botão de teste de e-mail faz

Quando você usa o botão de teste SMTP, o sistema aplica temporariamente a configuração de e-mail da sua empresa e tenta enviar um e-mail real. Isso ajuda a validar host, porta, usuário, senha, criptografia e remetente antes de liberar automações em produção.

### 19.5 Ordem sugerida de configuração

1. Preencher dados da empresa e validar impressões.
2. Configurar e testar SMTP.
3. Definir módulos e menus que ficarão visíveis.
4. Revisar limites de garantia, acompanhamento e metas comerciais.

### 19.6 Quem deve alterar configurações

- **Administrador:** perfil mais indicado para mudanças em SMTP, módulos, metas e regras operacionais.
- **Gestor:** pode participar da definição de metas, menus e automações.
- **Atendente e técnico:** normalmente apenas consultam, para evitar mudanças com impacto global.

### 19.7 Mensagens de permissão

Quando um usuário tentar executar uma ação para a qual não possui permissão, o sistema exibe um aviso na tela informando que a ação não é autorizada. Esse comportamento evita telas técnicas de erro e ajuda o usuário a entender que a limitação está relacionada ao perfil de acesso.

### 19.8 Mensagens amigáveis em falhas de operação

Durante operações como cadastrar, editar, excluir, salvar pagamento, enviar e-mail ou concluir uma ação, o sistema pode identificar falhas de conexão, sessão expirada, registro não encontrado, falta de permissão ou erro temporário do servidor. Nesses casos, o VetorOS exibe uma mensagem simples para o usuário, sem mostrar detalhes técnicos do Laravel.

| Situação | Mensagem esperada | O que fazer |
| --- | --- | --- |
| Internet instável ou servidor indisponível | Operação não concluída ou sem conexão com o servidor. | Verificar conexão e tentar novamente. |
| Sessão expirada | Sua sessão expirou. | Atualizar a página, entrar novamente se necessário e repetir a ação. |
| Sem permissão | Esta ação não é autorizada. | Solicitar liberação ao administrador se a ação fizer parte da função do usuário. |
| Registro removido ou não encontrado | Não foi possível encontrar o registro desta operação. | Atualizar a tela e conferir se outro usuário alterou ou removeu o item. |
| Falha ao enviar e-mail | Não foi possível enviar o e-mail agora. | Verificar internet, SMTP e usar o teste de e-mail nas configurações. |

Os detalhes técnicos continuam sendo registrados nos logs do sistema para análise do suporte ou da equipe técnica. O objetivo é proteger o usuário de mensagens internas difíceis de entender e orientar a próxima ação com clareza.

## 20. Gestão De Usuários

O sistema permite cadastrar, editar, excluir, ativar e inativar usuários. Também é possível definir permissões de acesso, adequando o uso conforme o perfil operacional.

- Administrador.
- Operador / atendente.
- Técnico.

As permissões ajudam a separar rotinas administrativas, atendimento, operação técnica e gestão do sistema. No formulário, o campo de funções do usuário usa seleção para evitar digitação livre e manter os perfis padronizados.

### 20.1 Exemplo prático de uso por perfil

- **Administrador:** configura empresa, SMTP, usuários, módulos e indicadores.
- **Operador / atendente:** abre OS, registra clientes, pagamentos e contatos.
- **Técnico:** atualiza andamento, diagnóstico, peças e observações técnicas.

### 20.2 Visibilidade entre perfis

A listagem e a edição de usuários seguem uma hierarquia de acesso para proteger contas de maior privilégio.

- **RootApp:** pode consultar a própria conta e os usuários operacionais da empresa.
- **Administrador:** visualiza administradores, atendentes e técnicos, mas não visualiza RootApp.
- **Atendente:** visualiza apenas a própria conta e usuários técnicos.
- **Técnico:** acessa apenas as funções liberadas para sua rotina operacional.

### 20.3 Técnico master

Ao cadastrar ou editar um usuário com função **Técnico**, administradores podem habilitar a opção **Técnico master**. Essa liberação permite que o técnico veja todas as ordens de serviço, não apenas as ordens atribuídas a ele. Quando a opção estiver desligada, o técnico continua restrito às próprias ordens.

### 20.4 Perfil e imagem do usuário

No menu do usuário existe a opção **Perfil**, usada para alterar o nome, trocar a senha e enviar uma imagem de perfil. A mesma imagem também pode ser definida no cadastro ou na edição de usuários, inclusive para técnicos.

As imagens aceitas são JPG, PNG ou WebP, com limite de 2 MB. Caso a pasta de armazenamento de avatares ainda não exista, o sistema cria automaticamente no primeiro envio.

Para selecionar a imagem, arraste o arquivo até a área tracejada ou clique nela para procurar no dispositivo. A prévia aparece antes do salvamento e pode ser removida pelo botão **×**. No cabeçalho do sistema, passe o mouse sobre o avatar para visualizar uma versão ampliada.

## 21. Aplicativos Auxiliares

O VetorOS possui uma área própria para baixar aplicativos Android que complementam a rotina da empresa. Ela fica no menu **Configurações > Aplicativos auxiliares** e mostra quais APKs estão disponíveis para instalação.

Cada app aparece com nome, descrição, arquivo, tamanho quando disponível e botão de download. Se o APK ainda não estiver publicado no servidor, o sistema exibe o status **Aguardando APK** e mantém o botão desabilitado para evitar instalação incorreta.

**Vetor Imagem**
App dedicado a localizar ordens de serviço e registrar imagens diretamente nelas. É útil para documentar recebimento, estado do equipamento, defeito e evidências do atendimento.

**Vetor Atendimento**
App de autoatendimento para pré-cadastro de clientes e consulta de orçamentos, agilizando tarefas rápidas da recepção e do balcão.

**Vetor Técnico**
App para técnicos consultarem atendimentos externos atribuídos, fazer check-in, preencher relatório/checklist, anexar imagens, registrar pagamento local e finalizar a visita.

**Controle de acesso**
O menu exige permissão de configurações. O uso de cada app continua respeitando login, empresa, perfil do usuário e permissões operacionais.

### 21.1 Como baixar e instalar

1. Acessar **Configurações > Aplicativos auxiliares**.
2. Conferir o app correto para a rotina desejada.
3. Clicar em **Baixar APK** quando o status estiver disponível.
4. Instalar no aparelho Android autorizado pela empresa.
5. Entrar com o mesmo usuário usado no VetorOS, respeitando o perfil de acesso.

### 21.2 Quando usar cada app

- **Recepção ou balcão:** usar Vetor Atendimento para cadastro rápido e consulta de orçamento.
- **Bancada ou conferência:** usar Vetor Imagem quando a principal necessidade for documentar a OS com fotos.
- **Atendimento externo:** usar Vetor Técnico para agenda, deslocamento, execução e encerramento em campo.

### 21.3 Cuidados operacionais

- Instalar APKs somente pelo link exibido no VetorOS da empresa.
- Manter usuários técnicos ativos e corretamente vinculados aos agendamentos.
- Conferir conexão, permissão de câmera e permissão de notificação no aparelho quando o app precisar desses recursos.
- Evitar compartilhar login entre colaboradores, pois ações, imagens, pagamentos e encerramentos ficam vinculados ao usuário autenticado.

## 22. Upload De Imagens

As ordens podem receber imagens enviadas pela própria interface do sistema ou por fluxo auxiliar de upload. Esse recurso é útil para documentar o estado de entrada, o defeito e as evidências do serviço executado.

Cada ordem aceita no máximo **oito imagens**, o que ajuda a documentar o atendimento sem deixar o cadastro excessivamente pesado.

No app técnico, as imagens podem ser anexadas diretamente no atendimento, respeitando o mesmo limite da ordem. O técnico deve usar esse recurso para evidências realmente úteis, como estado do equipamento, peça substituída, local de instalação ou comprovante visual do serviço.

O app de imagens continua disponível para equipes que desejam um fluxo dedicado apenas ao envio de fotos da ordem pelo celular. Ele é útil quando a operação separa recepção, bancada e registro visual do atendimento.

### 22.1 Quando usar imagens

- **Entrada do equipamento:** para documentar avarias, acessórios e estado físico.
- **Durante o reparo:** para registrar peças trocadas e pontos técnicos relevantes.
- **Saída:** para reforçar a evidência do serviço entregue.

### 22.2 Cuidados no envio pelo app técnico

- Enviar imagens somente quando houver conexão suficiente para concluir o upload.
- Evitar fotos repetidas ou sem relação com a ordem.
- Conferir se a imagem foi exibida na lista após o envio.
- Remover imagens enviadas por engano quando a permissão do usuário permitir.

## 23. Importação De Clientes Por CSV

O sistema permite importar clientes em lote por arquivo CSV ou TXT. O delimitador do arquivo é identificado automaticamente entre os formatos mais comuns, reduzindo trabalho manual na migração de base antiga.

- E-mails repetidos são aceitos na importação.
- O sistema tenta importar em lote e, se necessário, faz tratamento individual por linha.
- Ao final, a importação informa quantos clientes foram salvos e se houve linhas com erro.
- Datas precisam estar em formato consistente para evitar falhas durante a leitura do arquivo.

Antes de importar grandes volumes, vale revisar um arquivo de amostra com alguns registros para validar nomes de colunas, documentos e datas.

### 23.1 Quem deve fazer a importação

- **Administrador ou responsável pela implantação:** para validar qualidade da base antes de subir tudo.

## 24. Emissão Fiscal

O VetorOS não emite notas automaticamente nem exige contratação de API fiscal. A empresa pode emitir seus documentos pelo sistema oficial, prefeitura, Emissor Nacional ou serviço de sua preferência e manter os dados registrados junto da operação.

> **Links oficiais:** para serviços, o botão abre o Emissor Nacional da NFS-e. Para produtos, o Portal Nacional da NF-e é oficial para informações e consultas, mas não funciona como emissor web nacional. A NF-e deve ser emitida pelo software da empresa, emissor autorizado ou solução indicada pela SEFAZ estadual.

### 24.1 Como registrar uma NFS-e da ordem

1. Emita a NFS-e fora do VetorOS pelo emissor utilizado pela empresa.
2. Abra a ordem de serviço correspondente e escolha a opção de registro manual da nota.
3. Informe número, chave ou código de verificação, data de emissão, links disponíveis e observações.
4. Salve e confira se o documento ficou vinculado à ordem correta.

### 24.2 Como registrar uma NF-e da venda

1. Emita a NF-e de produtos fora do VetorOS.
2. Abra a venda correspondente e use a opção de registro manual da NF-e.
3. Informe os dados do documento e os links do DANFE ou XML, quando disponíveis.
4. Salve para manter o histórico fiscal associado à venda.

### 24.3 Consulta e arquivos

A listagem de notas permite consultar os registros vinculados às ordens e vendas. Como o fluxo é manual, o VetorOS não transmite, autoriza, cancela ou sincroniza documentos com órgãos fiscais.

### 24.4 Permissões e responsabilidade fiscal

- O registro fica disponível somente para usuários com a permissão correspondente.
- Confira o vínculo com a ordem ou venda antes de salvar.
- A responsabilidade pela conferência tributária, alíquotas, códigos fiscais e obrigações legais permanece com a empresa e sua contabilidade.

### 24.5 Configuração do modo manual

Em **Sistema e módulos > Fiscal**, habilite o módulo fiscal e os tipos de documento usados pela empresa. Sem a assinatura fiscal adicional, o modo exibido é **Manual com registro de comprovante** e os parâmetros automáticos ficam ocultos.

Quando o Root Admin libera a assinatura de emissão fiscal automática para a empresa, a opção **Automática pelas APIs governamentais** aparece nessa mesma tela, junto dos dados fiscais necessários. Ao retirar a liberação, o sistema volta a forçar o modo manual sem apagar os parâmetros fiscais já cadastrados.

## 25. Guia Rápido Dos Botões Mais Comuns

| Botão / ação | Onde aparece | O que faz | O que o sistema registra |
| --- | --- | --- | --- |
| Salvar | Cadastros em geral | Grava o formulário atual. | Atualização do registro e, em alguns casos, auditoria. |
| Editar | Listagens | Abre o item para alteração. | Somente ao confirmar o salvamento. |
| Excluir | Listagens e detalhes | Remove o item quando permitido. | Exclusão e, em vários módulos, log operacional. |
| Registrar pagamento | OS / Vendas | Lança recebimento. | Valor, forma, data e vínculo com caixa. |
| Enviar acompanhamento | OS / Acompanhamentos | Dispara contato manual com cliente. | Log do envio e último contato. |
| Pausar | Acompanhamentos | Interrompe a automação da OS. | Motivo e data da pausa. |
| Retomar | Acompanhamentos | Reativa a automação. | Retirada da pausa e retorno à fila quando elegível. |
| Concluir tarefa | Tarefas | Marca a pendência como tratada. | Log de tarefa concluída. |
| Registrar fiscal | OS / Vendas | Salva manualmente os dados de um documento emitido fora da integração. | Número, chave, data e usuário responsável. |
| Teste de e-mail | Sistema e módulos | Valida SMTP da sua empresa. | Tentativa real de envio com as credenciais configuradas. |
| Enviar ao técnico | Agendamentos | Disponibiliza a visita no app técnico do responsável. | Agenda vinculada ao técnico, à ordem e à empresa. |
| Check-in / Check-out | App técnico | Registra início e final do atendimento em campo. | Data, hora, observações e localização quando permitida. |
| Salvar relatório técnico | App técnico | Grava diagnóstico, solução e observações do atendimento. | Informações técnicas vinculadas à ordem de serviço. |

## 26. Boas Práticas De Uso

- Manter clientes e equipamentos sempre atualizados.
- Preencher corretamente defeito, acessórios e observações.
- Usar os contadores dos campos de texto; descrições e observações operacionais aceitam até 500 caracteres.
- Atualizar o status da ordem conforme a etapa real do atendimento.
- Registrar pagamentos e vendas no momento em que acontecerem.
- Abrir e fechar o caixa diariamente com conferência.
- Revisar despesas e diferenças de caixa no mesmo dia.
- Configurar e testar o SMTP antes de usar e-mails automáticos em produção.
- Revisar a aba Operacionais para decidir quais menus e automações devem ficar ativos.
- Deixar o acompanhamento automático desligado enquanto a operação ainda estiver em fase de ajuste.
- Usar relatórios para acompanhar desempenho, faturamento e pendências.
- Revisar diariamente Acompanhamentos, Tarefas e Garantia/Avaliações.
- Validar o portal do cliente com alguns atendimentos antes de divulgar em massa.
- Orientar a equipe sobre o papel de cada app: Autoatendimento para cadastros rápidos e orçamentos, Técnico para agenda em campo e Imagens para documentação visual da OS.
- Quando aparecer uma mensagem amigável de falha, repetir a ação apenas depois de conferir conexão, sessão e dados informados.

## 27. Suporte

Em caso de dúvidas de uso, configuração ou melhoria, mantenha este manual atualizado junto da versão instalada do sistema e utilize o canal de suporte definido pela empresa.

> Este manual foi pensado para treinamento, implantação, operação diária e apoio gerencial. Sempre que o sistema receber novos fluxos, telas ou automações, o ideal é atualizar também esta página para que o time continue operando com segurança.

### 27.1 Informações úteis ao solicitar suporte

- Informe a tela e a ação que estava executando.
- Anote a mensagem exibida e o horário aproximado da ocorrência.
- Confirme se o problema acontece novamente após atualizar a página.
- Não envie senhas, tokens, certificados digitais ou dados sensíveis em capturas de tela.
