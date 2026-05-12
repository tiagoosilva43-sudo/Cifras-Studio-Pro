# 📝 Cifras Studio - Histórico de Versões (Stable)

## Versão 2.1 (2026-05-12)

### 🐛 Correções Aplicadas

#### 1. Reconhecimento automático de acordes consecutivos
- **Problema**: Acordes escritos sem espaço entre os colchetes não eram reconhecidos corretamente
- **Solução**: Sistema agora reconhece corretamente acordes como `[C][G][Am][F]`
  - Exemplo: `[C][G][Am][F]` é automaticamente convertido para `[C] [G] [Am] [F]`
  - Correção aplicada em 3 pontos do código:
    1. `compilarCifra()` - Ao renderizar o documento final
    2. `processarConversao()` - Ao converter cifras no conversor automático
    3. `adicionarNovaParte()` - Ao salvar uma seção manualmente

#### 2. Cor padrão do seletor de cores
- **Problema**: A cor padrão era `#3b82f6` (azul), que não fazia parte das 8 cores pré-definidas
- **Solução**: Cor padrão agora é `#8a0000` (vermelho escuro), a primeira cor da paleta
- **Benefício**: Consistência visual e melhor experiência do usuário

### 💡 Benefícios
- ✅ Não é mais necessário adicionar espaços manualmente entre acordes
- ✅ Funciona tanto no conversor automático quanto na digitação manual
- ✅ Garante que todos os acordes sejam reconhecidos e exibidos corretamente no PDF
- ✅ Melhora significativa na experiência do usuário

### 🔧 Implementação Técnica
```javascript
// Código aplicado nos 3 pontos mencionados:
texto = texto.replace(/\]\[/g, '] [');
```

### 📊 Exemplos de Funcionamento

| Entrada | Processamento | Resultado |
|---------|---------------|-----------|
| `[C][G][Am][F]` | `[C] [G] [Am] [F]` | ✅ Todos reconhecidos |
| `[D][A][Bm][G]Refrão` | `[D] [A] [Bm] [G]Refrão` | ✅ Todos reconhecidos |
| `[Em][C][G][D]` | `[Em] [C] [G] [D]` | ✅ Todos reconhecidos |

---

## Versão 2.0 (2026-05-11)

### ✨ Versão Inicial Stable
- Interface limpa e minimalista
- Sistema completo de criação de cifras em 4 passos
- Conversor automático de cifras
- Seletor de cores customizado (8 cores)
- Drag & drop com Sortable.js
- Transposição de tom inteligente
- Geração de documento A4 com paginação automática
- Salvamento/carregamento de projetos (File System API)
- Modo escuro automático
- Layout responsivo para mobile
- Swipe gesture para abrir sidebar
- Exportação PDF diferenciada (Desktop: impressão / Mobile: download)

---

## 🎸 Como Usar o Cifras Studio

### 1️⃣ Dados da Música
Preencha as informações básicas:
- Título da música
- Autor/Banda
- Tom (ex: G, Am, C#)
- BPM (ex: 120)
- Compasso (ex: 4/4)

### 2️⃣ Criar Seções
1. Digite a **sigla** da seção (ex: V1, R, P, I)
2. Digite o **título** completo (ex: VERSO 1, REFRÃO, PONTE)
3. Escolha uma **cor** para identificação visual
4. Digite ou cole a cifra com acordes entre colchetes: `[C]Letra da [G]música`
5. **Dica**: Acordes consecutivos podem ser escritos juntos: `[C][G][Am][F]` ✅

#### Usando o Conversor Automático:
1. Clique em "Abrir Conversor"
2. Cole a cifra no formato tradicional (acordes em uma linha, letra na linha seguinte)
3. Clique em "Converter"
4. A cifra será convertida automaticamente para o formato do programa

### 3️⃣ Ordem e Dinâmicas
- Clique nas **bolinhas coloridas** para adicionar seções ao mapa
- **Arraste** para reordenar a sequência
- Adicione **comentários e dinâmicas** (ex: "Todos juntos", "Bateria forte")
- Marque opções:
  - **Mesclar repetição**: Une repetições consecutivas no mesmo balão
  - **Ocultar balão**: Remove a seção do PDF (útil para notas internas)

### 4️⃣ Visualizar e Imprimir
- Visualize o documento final em formato A4 profissional
- **Transponha o tom** com os botões +½ e -½
- **Salve o projeto** para editar depois (formato .json)
- **Imprima ou salve como PDF**:
  - Desktop: Abre diálogo de impressão
  - Mobile: Salva PDF automaticamente

---

## 💾 Salvamento de Projetos

### Salvar Projeto
- Clique em "💾 Salvar Projeto"
- Escolha o local e nome do arquivo
- O arquivo será salvo em formato .json
- Próximas vezes: sobrescreve automaticamente o mesmo arquivo

### Carregar Projeto
- Clique em "Carregar Projeto Salvo"
- Selecione o arquivo .json
- Todos os dados serão restaurados

---

## 📱 Recursos Mobile

### Gestos:
- **Swipe da borda esquerda**: Abre o menu de navegação
- **Swipe para esquerda**: Fecha o menu

### Diferenças:
- Botão de impressão vira "Salvar PDF"
- Layout otimizado para telas pequenas
- Páginas A4 escaladas automaticamente
- Zoom bloqueado para melhor experiência

---

## ⌨️ Atalhos de Teclado (Desktop)

Atualmente não implementados na versão Stable.
Disponíveis na versão Testes (avançada).

---

## 🎨 Paleta de Cores Padrão

1. 🔴 Vermelho escuro (`#8a0000`)
2. 🟠 Laranja escuro (`#995c00`)
3. 🟢 Verde escuro (`#0a5700`)
4. 🔵 Azul petróleo (`#007070`)
5. 🔵 Azul marinho (`#001773`)
6. 🟣 Roxo escuro (`#66005e`)
7. 🟡 Amarelo oliva (`#968a00`)
8. ⚫ Cinza escuro (`#4e5e63`)

---

## 🔧 Suporte Técnico

### Navegadores Suportados:
- ✅ Chrome/Edge (recomendado)
- ✅ Firefox
- ✅ Safari (Desktop e iOS)
- ✅ Opera

### Requisitos:
- JavaScript habilitado
- Resolução mínima: 320px (mobile)
- Conexão com internet (para carregar fontes)

---

## 📄 Licença
Cifras Studio v2.1 - Ferramenta profissional para criação de cifras musicais
