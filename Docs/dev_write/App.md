# Estrutura do MLB

O MLB está dividido em duas grandes partes.

1. Primeira Camada
   
Corresponde ao ecrã exibido ao iniciar a aplicação. É constituído por dois elementos visuais principais, com destaque para a Roda.

A Roda
 * Localização no código: demo/contents/wheel
 * Divisão de gavetas/menus:

A. Launch App
Inicialização rápida da aplicação principal.

B. LLM Installation
Permite descarregar e gerir modelos de linguagem para utilização 100% local.
> Requisitos da Interface: Cada modelo deve apresentar claramente os requisitos de instalação: espaço em disco, memória RAM e GPU recomendada.
> 
 * Qwen
   * Qwen3-235B-A22B
   * Qwen3-32B
   * Qwen3-14B
   * Qwen3-8B
   * Qwen3-4B
   * Qwen3-1.7B
   * Qwen3-0.6B
 * DeepSeek
   * Deepseek-r1:1.5b
   * Deepseek-r1:7b
   * Deepseek-r1:8b
   * Deepseek-r1:14b
   * Deepseek-r1:32b
   * Deepseek-r1:70b
   * Deepseek-r1:671b
   * Deepseek-v4-flash
   * Deepseek-v3
   * Deepseek-coder-v2
   * Deepseek-coder
 * Kimi
   * Kimi-k2.6
   * Kimi-k2.7-code
   * 
C. Use API Key
Interface simples e direta para integração via API externa.
 * Campos do formulário:
   * API Key
   * Nome do Modelo
   * URL / Link da Fornecedora
 * Ação: Botão para guardar credenciais.
   
D. Connect Agents
Integração com agentes externos.
 * Codex
   > Funcionamento: Abre uma página de autenticação no navegador para efetuar login direto na conta da OpenAI.
   


2. Segunda Camada (Launch App)
Ao abrir a aplicação (Launch App), o ecrã surge estruturado em 3 colunas verticais (proporção 1/4 - 2/4 - 1/4), repletas de funcionalidades.
A. Painel Esquerdo (1/4 do Ecrã) — Navegação e Customização
Serve para navegar entre conversas e personalizar as definições do LLM.
 * Componente base: demo/contents/branched_menu
 * Categorias:
   
1. Personalização
 * Rails: Instruções de leitura obrigatória pelo LLM antes de gerar respostas.
   > Ativação: Funciona via drag and drop de um ficheiro .zip contendo um INSTRUCTIONS.md no interior.
   
 * Language: Mudança global de idioma da aplicação.
   * Idiomas disponíveis: Francês, Português (PT-PT), Inglês, Chinês e Espanhol.
     
 * Connectors: Integrações de dados e serviços externos.
   * Suportados atualmente: GitHub e Gmail.
     
 * Temperatura: Ajuste fino dos hiperparâmetros de geração através de sliders elásticos.
   * Componente: demo/contents/elastic_slider
   * Controlos: Temperature, Top-K, Top-P e Repeat Penalty.
     
2. Codex
 * Gestão e histórico de chats específicos do agente Codex.
3. Chats
 * Gestão e histórico de conversas convencionais.
B. Painel Central (2/4 do Ecrã) — Canal e Área de Trabalho
Painel dinâmico onde é exibido o conteúdo do canal ou conversa selecionada.
Barra de Prompt e Controlos Superiores
 * Seletor de Nível de Esforço (Effort):
   * Adaptável/Modular: Altera-se consoante as capacidades do modelo ativo.
   * Chat com Agentes (Codex): Níveis avançados — Light, Medium, High, Extra High e Ultra Max.
   * Modelos sem suporte: O painel esconde/desativa automaticamente os controlos irrelevantes.
 * Seletor de Modelos (Glide Select):
   * Componente: demo/contents/glide_select
   * Modo Chat Normal: Lista todos os modelos instalados localmente e/ou modelos Cloud configurados via API Key.
   * Modo Agentes / Codex: Deteta automaticamente os modelos disponíveis na CLI do agente (ex: 5.6 luna, 5.6 terra, 5.6 sol, 6 astra, etc.).
Indicador de Processamento
 * Lattice Loader:
   * Componente: demo/contents/lattice_loader
   * Comportamento: É exibido enquanto o modelo está a processar/pensar.
   * Animação de Conclusão: Gera um padrão gráfico aleatório e dinâmico no final de cada resposta.
   * 
C. Painel Direito (1/4 do Ecrã) — Thinking Orb
Elemento visual interativo e reativo.
 * Componente: demo/contents/thinking_orb
 * Função: Reage e interage em tempo real com o estado de raciocínio e ações do LLM.
