# 🎸 Cifras Studio

<div align="center">

![Version](https://img.shields.io/badge/version-2.1-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

**Ferramenta profissional para criação e formatação de cifras musicais**

[Demo ao Vivo](#) • [Documentação](#-como-usar) • [Reportar Bug](../../issues) • [Solicitar Recurso](../../issues)

</div>

---

## 📖 Sobre o Projeto

**Cifras Studio** é uma aplicação web completa para músicos, bandas e ministérios de louvor que precisam criar, organizar e imprimir cifras de forma profissional. Com interface intuitiva e recursos avançados, você pode criar documentos A4 prontos para impressão em minutos.

### ✨ Principais Recursos

- 🎵 **Criação de Cifras Profissionais** - Sistema completo em 4 passos
- 🔄 **Conversor Automático** - Converte cifras do formato tradicional
- 🎨 **Organização Visual** - 8 cores para identificar seções
- 🎹 **Transposição de Tom** - Mude o tom com um clique
- 📄 **Exportação PDF** - Documentos A4 prontos para impressão
- 💾 **Salvamento de Projetos** - Salve e carregue seus trabalhos
- 📱 **Responsivo** - Funciona perfeitamente em desktop e mobile
- 🌙 **Modo Escuro** - Tema automático baseado no sistema
- ⚡ **Sem Instalação** - Funciona direto no navegador

---

## 🚀 Versões Disponíveis

### 📦 Stable (Recomendado)
Versão estável e testada, ideal para uso em produção.
- Interface limpa e minimalista
- Máxima compatibilidade
- Performance otimizada
- **[Acessar Stable →](Stable/)**

### 🧪 Testes (Experimental)
Versão com recursos avançados e design moderno.
- Design glassmorphism
- Animações e micro-interações
- Auto-save e atalhos de teclado
- Recursos experimentais
- **[Acessar Testes →](Testes/)**

---

## 🎯 Como Usar

### 1️⃣ Dados da Música
Preencha as informações básicas:
- Título da música
- Autor/Banda
- Tom (ex: G, Am, C#)
- BPM e Compasso

### 2️⃣ Criar Seções
- Digite a **sigla** (V1, R, P, I)
- Digite o **título** (VERSO 1, REFRÃO, PONTE)
- Escolha uma **cor** para identificação
- Digite a cifra: `[C]Letra da [G]música`

💡 **Dica**: Use o conversor automático para cifras tradicionais!

### 3️⃣ Ordem e Dinâmicas
- Clique nas bolinhas coloridas para montar a estrutura
- Arraste para reordenar
- Adicione comentários (dinâmicas, observações)
- Configure repetições e ocultações

### 4️⃣ Visualizar e Imprimir
- Visualize o documento A4 profissional
- Transponha o tom se necessário
- Salve o projeto para editar depois
- Imprima ou salve como PDF

---

## 💻 Instalação

### Opção 1: Download Direto
1. Baixe os arquivos da pasta `Stable/` ou `Testes/`
2. Abra o arquivo `index.html` no navegador
3. Pronto! Não precisa de servidor

### Opção 2: Clone o Repositório
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/cifras-studio.git

# Entre na pasta
cd cifras-studio

# Abra no navegador
# Stable: abra Stable/index.html
# Testes: abra Testes/index.html
```

### Opção 3: GitHub Pages
Acesse diretamente online (se configurado):
- **Stable**: `https://seu-usuario.github.io/cifras-studio/Stable/`
- **Testes**: `https://seu-usuario.github.io/cifras-studio/Testes/`

---

## 🛠️ Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilização moderna e responsiva
- **JavaScript (ES6+)** - Lógica e interatividade
- **[Sortable.js](https://sortablejs.github.io/Sortable/)** - Drag and drop
- **[jsPDF](https://github.com/parallax/jsPDF)** - Geração de PDF (mobile)
- **[html2canvas](https://html2canvas.hertzen.com/)** - Captura de tela (mobile)
- **File System Access API** - Salvamento nativo de arquivos

---

## 📱 Compatibilidade

### Navegadores Suportados
| Navegador | Desktop | Mobile |
|-----------|---------|--------|
| Chrome    | ✅ v90+ | ✅ v90+ |
| Edge      | ✅ v90+ | ✅ v90+ |
| Firefox   | ✅ v88+ | ✅ v88+ |
| Safari    | ✅ v14+ | ✅ v14+ |
| Opera     | ✅ v76+ | ✅ v76+ |

### Dispositivos Testados
- ✅ Desktop (Windows, macOS, Linux)
- ✅ Tablets (iPad, Android)
- ✅ Smartphones (iOS, Android)

---

## 🎨 Paleta de Cores

As 8 cores pré-definidas para organização visual:

| Cor | Hex | Uso Sugerido |
|-----|-----|--------------|
| 🔴 Vermelho | `#8a0000` | Versos |
| 🟠 Laranja | `#995c00` | Pré-refrão |
| 🟢 Verde | `#0a5700` | Refrão |
| 🔵 Azul Petróleo | `#007070` | Ponte |
| 🔵 Azul Marinho | `#001773` | Introdução |
| 🟣 Roxo | `#66005e` | Final |
| 🟡 Amarelo | `#968a00` | Solo |
| ⚫ Cinza | `#4e5e63` | Observações |

---

## 📋 Funcionalidades Detalhadas

### 🎵 Sistema de Cifras
- Reconhecimento automático de acordes
- Suporte a acordes complexos (7M, sus4, dim, aug, etc.)
- Acordes com baixo invertido (C/G, Am/F#)
- Espaçamento automático entre acordes consecutivos

### 🔄 Conversor Automático
- Converte cifras do formato tradicional
- Detecta linhas de acordes automaticamente
- Mescla acordes com letras
- Preserva formatação original

### 🎹 Transposição de Tom
- Transposição por semitons (+½ / -½)
- Mantém tensões e extensões
- Preserva baixos invertidos
- Suporte a sustenidos e bemóis

### 📄 Geração de Documentos
- Formato A4 profissional
- Paginação automática em 2 colunas
- Cabeçalho com informações da música
- Mapa visual da estrutura
- Rodapé com numeração de páginas

### 💾 Salvamento de Projetos
- Formato JSON leve e portátil
- Salvamento nativo (File System API)
- Sobrescrita automática
- Compatibilidade entre versões

### 📱 Recursos Mobile
- Layout responsivo otimizado
- Swipe gesture para menu
- Geração de PDF nativa
- Zoom bloqueado para melhor UX
- Páginas A4 escaladas automaticamente

---

## 🔄 Changelog

### [2.1] - 2026-05-12

#### 🐛 Correções
- **Acordes consecutivos**: Sistema agora reconhece `[C][G][Am]` automaticamente
- **Cor padrão**: Seletor agora inicia com a primeira cor da paleta

#### 📝 Detalhes
- Adiciona espaçamento automático entre acordes sem espaço
- Corrige inicialização do seletor de cores
- Melhora experiência do usuário

### [2.0] - 2026-05-11

#### 🎉 Lançamento Inicial
- Sistema completo de criação de cifras
- Conversor automático
- Transposição de tom
- Exportação PDF
- Modo escuro
- Versão mobile

[Ver changelog completo →](CHANGELOG.md)

---

## 🤝 Como Contribuir

Contribuições são sempre bem-vindas! Aqui está como você pode ajudar:

1. **Fork** o projeto
2. Crie uma **branch** para sua feature (`git checkout -b feature/MinhaFeature`)
3. **Commit** suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. **Push** para a branch (`git push origin feature/MinhaFeature`)
5. Abra um **Pull Request**

### 💡 Ideias de Contribuição
- 🐛 Reportar bugs
- ✨ Sugerir novas funcionalidades
- 📝 Melhorar documentação
- 🌍 Adicionar traduções
- 🎨 Melhorar design
- ⚡ Otimizar performance

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

```
MIT License

Copyright (c) 2026 Cifras Studio

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 👨‍💻 Autor

**Tiago Silva**

- GitHub: [@tiagoosilva43-sudo](https://github.com/tiagoosilva43-sudo)
- Email: tiago.o.silva43@gmail.com

---

## 🙏 Agradecimentos

- [Sortable.js](https://sortablejs.github.io/Sortable/) - Biblioteca de drag and drop
- [jsPDF](https://github.com/parallax/jsPDF) - Geração de PDF
- [html2canvas](https://html2canvas.hertzen.com/) - Captura de tela
- [Google Fonts](https://fonts.google.com/) - Fonte Inter
- Comunidade de músicos que testaram e deram feedback

---

## 📞 Suporte

Encontrou um problema? Tem uma sugestão?

- 🐛 [Reportar Bug](../../issues/new?labels=bug)
- ✨ [Solicitar Recurso](../../issues/new?labels=enhancement)
- 💬 [Discussões](../../discussions)
- 📧 Email: tiago.o.silva43@gmail.com

---

## ⭐ Mostre seu Apoio

Se este projeto te ajudou, considere dar uma ⭐ no repositório!

---

<div align="center">

**Feito com ❤️ para a comunidade musical**

[⬆ Voltar ao topo](#-cifras-studio)

</div>
