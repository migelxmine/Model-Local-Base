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
   
2 segunda camada. ao abrir a app (lunch app) viras um ecra cheio de funcjonalidades e o ecra dividido em 3 (especificamente 4/4, 1/4 esquerdo do ecrã serve para navegares por chast e cistumizares o llm, tem modelo em  demo/contents/branched_menu, q esta dividido em 2/3 (se aplicavel) categorias sendo:

- Personalização
  - Rails (aqui basicamente é uma (ou varias) instruvoes q o llm lê obrigatpriamente sempre se ligado antes de pensar (tens de drag and drop um .zip q contenga um (INSTRUCTIONS.md) debtro)
  - Language (permite te mudares a lingua da app (frances, pt pt, ingles, chines e espanhol)
  - Connectors (Aqui por enquanto Github e Gmail)
  - Temperatura (Aqui tens varios sliders (demo/contents/elastic_slider) com temperatura 
- Codex
  - Chats
- Chats
  
2/4 do ecra estao no meio q é o painel do respectivo canal (canel sao os coisos dentro das categorias), ao estar um chat a barra de prompt vem com outras coisas em cima (effort se aplicavel e modular (modular no sentidp de, se há modelos on off nao faz sentido estar com dedativado baixo medio alto, e tmb como no chat de agents ao usar o codex baixo medio alto ja q é Light Medium Hight Extra high Ultra max) em chat normal ao lado sessa barrinha uma cena q abre uma lista de modleos (demo/contents/glide_select) com todos os modelos instalados (se aplicavel o da vloud se guardasses a apj o modleo e etc) ja em agentes essa lista, os llm muda para os ll. disponivel nesse cli (no caso do vodez aparece 5.6 luna 5.6 terra 5.6 sol 6 astra etc todos os q sao detectados) onde ele escreve sempre q pensa aparece isto (demo/contents/lattice_loader, com um mod q ao completar faz um padrao random nao fixo)

1/4 do ecra direito é thinking orb (demo/contents/thinking_orb) q reage e interage oq o llm esta a fazer

