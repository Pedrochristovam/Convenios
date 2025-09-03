# Convenios
Visão Geral do Funcionamento
O sistema ConvênioIA foi criado para ser uma plataforma completa e intuitiva que transforma a análise manual e demorada de convênios em um processo automatizado, inteligente e rastreável. O fluxo de trabalho é centrado em um pipeline visual que orienta o usuário desde o upload do documento até a geração do relatório final.

1. Estrutura de Navegação (Layout)
A interface principal é organizada com uma barra de navegação lateral (sidebar) que dá acesso rápido a todas as áreas-chave do sistema:

Dashboard: Sua central de comando, com uma visão geral de tudo.
Nova Análise: Ponto de partida para analisar um novo convênio.
Workflows N8N: Uma área avançada para personalizar a proteção de dados com IA.
Relatórios: Onde você visualiza e exporta os resultados detalhados.
Configurações: Onde você define as regras de negócio do sistema.
A barra lateral também exibe um resumo em tempo real do status dos convênios e fluxos de trabalho, mantendo você informado a todo momento.

2. Painel
Ao entrar no sistema, você é recebido pelo Dashboard, que oferece uma visão panorâmica e gerencial:

Cartões de Status: Quatro cartões no topo mostram os números mais importantes: total de convênios, quantos estão concluídos, em análise ou com pendências.
Convênios Recentes: Uma lista dinâmica exibe os últimos documentos enviados. Para cada um, você vê o nome, os dados de upload e um selo colorido (badge) indicando seu status atual (Ex: "Em Análise", "Concluído"). A partir daqui, você pode navegar diretamente para a tela de análise de qualquer convênio.
Status do Pipeline: Um gráfico visual mostra em quais das 3 etapas (Análise, Validação, Relatório) os convênios estão concentrados, ajudando a identificar gargalos no processo.
3. Nova Análise (Upload)
É aqui que a mágica começa:

Informações Básicas: Você preenche o nome e o número do convênio.
Upload do Documento: Uma área de "arrastar e soltar" (arrastar e soltar) permite que você envie o arquivo PDF. O sistema foi projetado para lidar com arquivos grandes (600-900 páginas). Ele exibe o nome e o tamanho do arquivo selecionado.
Iniciar Análise: Ao clicar, o sistema exibe uma tela de progresso, informando que está fazendo o upload e preparando o ambiente. Em seguida, você é redirecionado automaticamente para a tela de Análise .
4. Análise em Tempo Real (Pipeline Visual)
Esta é a tela central para acompanhar o andamento de um convênio específico. Ela é dividida em:

Pipeline Visual: No topo, as 3 etapas da análise são exibidas visualmente. Cada etapa muda de acordo com seu status:
Azul (Processando): A IA está trabalhando.
Verde (Concluído): A etapa foi finalizada com sucesso.
Amarelo (Pendente): A etapa concluída, mas há avisos ou informações faltando (com base nas suas configurações).
Vermelho (Erro): Ocorreu um erro na remoção ou validação.
Resultados da Análise: À medida que a IA processa o documento, um resumo dos dados extraídos aparece em tempo real (ex: "15 Notas Fiscais descobertas", "3 Processos Licitatórios").
5. Workflows N8N (Inteligência Personalizável)
Esta é a funcionalidade mais poderosa, que torna o sistema "treinável":

Objetivo: Permitir que você crie fluxos de extração personalizados usando a ferramenta N8N, integrando-a com a IA de sua preferência.
Como Funciona:
Você cria um "Novo Workflow", dando um nome (ex: "Extração para Convênios de Saúde").
Você insere a URL do Webhook do seu fluxo no N8N.
Você define quais campos deseja extrair (selecionando em uma lista ou adicionando campos personalizados).
Você pode escrever um prompt de IA específico para orientar a proteção (ex: "Extraia apenas notas fiscais de serviços e ignore as de produtos").
Na Prática: Quando um novo convênio é desenvolvido, o sistema verifica se existe um fluxo de trabalho ativo para aquele tipo de documento. Se houver, ele envia o arquivo para o seu N8N em vez de usar o fluxo padrão. Isso lhe dá controle total sobre o processo de degradação.
6. Relatórios
Após a conclusão da análise, os resultados ficam disponíveis aqui:

Visualização em Tela: Você seleciona um convênio e vê um relatório completo e bem estruturado, com frascos transparentes para:
Resumo executivo.
Tabela de Notas Fiscais.
Tabela de Extratos Bancários.
Tabela de Processos Licitatórios.
Cada item extraído indica a página do documento original onde foi encontrado.
Exportação: Com um clique, você pode exportar o relatório completo para Excel (ideal para análise de dados) ou PDF (para arquivamento e compartilhamento).
7. Configurações
Nesta tela, você define como "regras do jogo" para o sistema, personalizando o que é considerado obrigatório ou pendente:

Campos Obrigatórios: Para cada tipo de documento (Notas Fiscais, Extratos, etc.), você marca quais campos são essenciais. Se a IA não encontrar um campo marcado como obrigatório, o status da análise ficará "amarelo" (pendente).
Regras de Validação: Você pode definir regras mais específicas, como "o valor mínimo de uma nota fiscal é R$ 1,00" ou "só são aceitas licitações da modalidade pregão". Isso refina a validação automática e a precisão dos alertas.
Em resumo, o ConvênioIA automatiza o trabalho pesado, oferece visibilidade total do processo e permite que sua equipe ajuste as regras de extração e validação de forma flexível, garantindo que o sistema evolua junto com suas necessidades.
