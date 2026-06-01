# 🎨 Fundo Mágico

> Transforme suas ideias em backgrounds incríveis com o poder da IA. Descreva o que você imagina e veja a magia acontecer.

## 📋 Sobre o Projeto

**Fundo Mágico** é uma aplicação web que utiliza inteligência artificial para gerar backgrounds CSS personalizados. Através de simples descrições em linguagem natural, o sistema cria código HTML e CSS pronto para usar em seus projetos.

### ✨ Principais Características

- 🤖 **Geração por IA**: Descreva o background que deseja e deixe a IA trabalhar
- 💻 **Código Reutilizável**: Obtenha HTML e CSS prontos para copiar e colar
- 👁️ **Preview em Tempo Real**: Veja o resultado imediatamente na tela
- 📱 **Design Responsivo**: Interface otimizada para desktop e mobile
- ⚡ **Rápido e Intuitivo**: Interface simples e fácil de usar

## 🚀 Como Funciona

1. **Descreva**: Digite uma descrição detalhada do background que você deseja
2. **Gere**: Clique em "Gerar Background Mágico"
3. **Veja**: A IA processa e gera o código HTML/CSS
4. **Copie**: Use o código gerado em seus projetos

### Exemplo de Descrição
```
Um gradiente suave que vai do azul claro até o azul escuro
```

## 🛠️ Tecnologias Utilizadas

- **Frontend**
  - HTML5
  - CSS3 (com suporte responsivo)
  - JavaScript (ES6+)
  - Google Fonts (Roboto Mono)

- **Backend/API**
  - n8n (para orquestração da IA)
  - Claude/GPT (para geração de backgrounds)

## 📁 Estrutura do Projeto

```
projeto-fundo-magico/
├── index.html              # Página principal
├── README.md               # Este arquivo
└── src/
    ├── css/
    │   ├── reset.css       # Reset de estilos padrão
    │   ├── estilos.css     # Estilos principais
    │   └── responsivo.css  # Estilos responsivos
    ├── js/
    │   └── index.js        # Lógica da aplicação
    └── imagens/
        └── bg.JPG          # Imagens do projeto
```

## 💡 Como Usar

### Requisitos
- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Conexão com a internet

### Passo a Passo

1. **Abra o projeto**: Abra o arquivo `index.html` em seu navegador
2. **Digite uma descrição**: No campo de texto, descreva o background desejado
3. **Clique em "Gerar Background Mágico"**: A requisição será enviada para a API
4. **Aguarde o processamento**: Uma animação de carregamento aparecerá
5. **Copie o código**: Os códigos HTML e CSS aparecerão prontos para usar

## 🔧 Fluxo Técnico

```
Usuário digita descrição
          ↓
    Form valida entrada
          ↓
   Requisição POST para n8n
          ↓
    IA gera HTML/CSS
          ↓
    Resposta recebida
          ↓
    Preview renderizado
          ↓
    Código exibido ao usuário
```

## 📝 Estrutura de Requisição/Resposta

### Requisição (POST)
```json
{
  "descriptionValue": "Um gradiente suave que vai do azul claro até o azul escuro"
}
```

### Resposta
```json
{
  "html": "<div class=\"magic-background\"></div>",
  "css": ".magic-background { background: linear-gradient(...); }"
}
```

## 🎯 Detalhes de Implementação

### JavaScript (`src/js/index.js`)
O arquivo JavaScript gerencia:
- **Validação de formulário**: Impede envio vazio
- **Estado de carregamento**: Mostra indicador durante requisição
- **Comunicação com API**: Envia requisição POST para n8n
- **Renderização**: Exibe HTML/CSS e aplica estilos dinamicamente
- **Tratamento de erros**: Captura e exibe mensagens de erro

### CSS Dinâmico
O CSS gerado pela IA é inserido dinamicamente na página através de uma tag `<style>`, permitindo visualização imediata do resultado.

## 🌐 API n8n

O projeto utiliza um webhook n8n para processar requisições:
```
https://jasonsanoliver.app.n8n.cloud/webhook/30e0be00-c884-4e64-8b24-bb0abac748fc
```

## 📱 Responsividade

O projeto inclui breakpoints responsivos para diferentes tamanhos de tela:
- Desktop (> 1024px)
- Tablet (768px - 1024px)
- Mobile (< 768px)

## ⚠️ Limitações e Considerações

- Requer conexão com internet ativa
- Dependência da disponibilidade do webhook n8n
- Limites de taxa podem ser aplicados pela API
- Qualidade do resultado depende da descrição fornecida

## 🔮 Possíveis Melhorias Futuras

- [ ] Histórico de backgrounds gerados
- [ ] Salvar e carregar favoritos
- [ ] Exportar como arquivo CSS/HTML
- [ ] Temas presets para inspiração
- [ ] Modo offline com templates locais
- [ ] Sistema de feedback para melhorar geração

## 📄 Licença

Este projeto é parte do programa "Semana do Zero ao Programador Contratado".

## 👤 Autor

Desenvolvido com VSCode durante a Semana do Zero ao Programador Contratado por Jason Santana Oliveira

---

**Aproveite e crie backgrounds mágicos!** ✨
