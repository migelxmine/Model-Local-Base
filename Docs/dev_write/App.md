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
   
