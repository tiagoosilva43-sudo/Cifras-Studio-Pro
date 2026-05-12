# 🤝 Guia de Contribuição

Obrigado por considerar contribuir com o **Cifras Studio**! Este documento fornece diretrizes para contribuir com o projeto.

## 📋 Índice

- [Código de Conduta](#código-de-conduta)
- [Como Posso Contribuir?](#como-posso-contribuir)
- [Processo de Desenvolvimento](#processo-de-desenvolvimento)
- [Padrões de Código](#padrões-de-código)
- [Mensagens de Commit](#mensagens-de-commit)
- [Pull Requests](#pull-requests)

---

## 📜 Código de Conduta

Este projeto adota um Código de Conduta que esperamos que todos os participantes sigam. Por favor, leia o código completo para entender quais ações serão e não serão toleradas.

### Nossos Padrões

- ✅ Usar linguagem acolhedora e inclusiva
- ✅ Respeitar pontos de vista e experiências diferentes
- ✅ Aceitar críticas construtivas graciosamente
- ✅ Focar no que é melhor para a comunidade
- ❌ Usar linguagem ou imagens sexualizadas
- ❌ Fazer comentários insultuosos ou depreciativos
- ❌ Assédio público ou privado

---

## 🎯 Como Posso Contribuir?

### 🐛 Reportando Bugs

Antes de criar um relatório de bug, verifique se o problema já não foi reportado. Se você encontrar um bug:

1. **Use o template de issue** para bugs
2. **Descreva o problema** claramente
3. **Passos para reproduzir** o bug
4. **Comportamento esperado** vs **comportamento atual**
5. **Screenshots** se aplicável
6. **Ambiente**: navegador, versão, sistema operacional

**Exemplo de relatório de bug:**
```markdown
**Descrição do Bug**
Os acordes consecutivos [C][G][Am] não são reconhecidos.

**Passos para Reproduzir**
1. Vá para o Passo 2
2. Digite '[C][G][Am]Letra'
3. Salve a seção
4. Vá para o Passo 4
5. Observe que apenas [C] aparece

**Comportamento Esperado**
Todos os três acordes deveriam aparecer: [C] [G] [Am]

**Screenshots**
[Anexar screenshot]

**Ambiente**
- Navegador: Chrome 120
- SO: Windows 11
- Versão: Stable 2.0
```

### ✨ Sugerindo Melhorias

Sugestões de melhorias são sempre bem-vindas! Para sugerir uma melhoria:

1. **Use o template de issue** para features
2. **Descreva a funcionalidade** detalhadamente
3. **Explique por que** seria útil
4. **Forneça exemplos** de uso
5. **Considere alternativas** se houver

### 📝 Melhorando a Documentação

Documentação clara é essencial! Você pode ajudar:

- Corrigindo erros de digitação
- Melhorando explicações
- Adicionando exemplos
- Traduzindo para outros idiomas
- Criando tutoriais em vídeo

### 💻 Contribuindo com Código

1. **Fork** o repositório
2. **Clone** seu fork localmente
3. **Crie uma branch** para sua feature
4. **Faça suas alterações**
5. **Teste** suas alterações
6. **Commit** seguindo os padrões
7. **Push** para seu fork
8. **Abra um Pull Request**

---

## 🔄 Processo de Desenvolvimento

### Estrutura do Projeto

```
cifras-studio/
├── Stable/              # Versão estável
│   ├── index.html
│   ├── script.js
│   ├── style.css
│   └── CHANGELOG.md
├── Testes/              # Versão experimental
│   ├── index.html
│   ├── script.js
│   ├── style.css
│   └── CHANGELOG.md
├── Projetos/            # Exemplos de projetos (não versionado)
├── README.md
├── CHANGELOG.md
├── LICENSE
└── CONTRIBUTING.md
```

### Branches

- `main` - Código de produção estável
- `develop` - Branch de desenvolvimento
- `feature/*` - Novas funcionalidades
- `fix/*` - Correções de bugs
- `docs/*` - Melhorias na documentação

### Workflow

1. **Sempre trabalhe em uma branch separada**
   ```bash
   git checkout -b feature/minha-feature
   ```

2. **Mantenha commits pequenos e focados**
   ```bash
   git add arquivo-modificado.js
   git commit -m "feat: adiciona validação de acordes"
   ```

3. **Sincronize com a main regularmente**
   ```bash
   git fetch origin
   git rebase origin/main
   ```

4. **Teste antes de fazer push**
   - Teste em diferentes navegadores
   - Teste em mobile
   - Verifique o console por erros

---

## 📐 Padrões de Código

### JavaScript

```javascript
// ✅ BOM
function transporAcorde(acorde, semitons) {
    if (!acorde) return '';
    
    const nota = extrairNota(acorde);
    const novaNota = transporNota(nota, semitons);
    
    return acorde.replace(nota, novaNota);
}

// ❌ RUIM
function t(a,s){if(!a)return '';let n=e(a);let nn=tn(n,s);return a.replace(n,nn);}
```

**Regras:**
- Use `const` e `let`, evite `var`
- Nomes descritivos para variáveis e funções
- Comentários em português para lógica complexa
- Indentação de 4 espaços
- Ponto e vírgula obrigatório
- Aspas simples para strings

### CSS

```css
/* ✅ BOM */
.botao-primario {
    background: var(--cor-primaria);
    color: white;
    padding: 12px 24px;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.botao-primario:hover {
    background: var(--cor-primaria-hover);
    transform: translateY(-2px);
}

/* ❌ RUIM */
.btn{background:#3b82f6;color:#fff;padding:12px 24px;}
```

**Regras:**
- Use variáveis CSS para cores e valores reutilizáveis
- Classes em kebab-case
- Agrupe propriedades relacionadas
- Comentários para seções importantes
- Mobile-first quando aplicável

### HTML

```html
<!-- ✅ BOM -->
<button 
    type="button" 
    class="btn-primario" 
    onclick="salvarProjeto()"
    aria-label="Salvar projeto"
>
    💾 Salvar Projeto
</button>

<!-- ❌ RUIM -->
<button onclick="salvarProjeto()">Salvar</button>
```

**Regras:**
- Semântica HTML5
- Atributos de acessibilidade (aria-*)
- Indentação consistente
- Comentários para seções complexas

---

## 📝 Mensagens de Commit

Seguimos o padrão [Conventional Commits](https://www.conventionalcommits.org/).

### Formato

```
<tipo>(<escopo>): <descrição curta>

<descrição detalhada (opcional)>

<rodapé (opcional)>
```

### Tipos

- `feat`: Nova funcionalidade
- `fix`: Correção de bug
- `docs`: Mudanças na documentação
- `style`: Formatação, ponto e vírgula, etc (sem mudança de código)
- `refactor`: Refatoração de código
- `perf`: Melhoria de performance
- `test`: Adição ou correção de testes
- `chore`: Tarefas de manutenção

### Exemplos

```bash
# Feature
git commit -m "feat(conversor): adiciona suporte a acordes com 9ª"

# Bug fix
git commit -m "fix(pdf): corrige paginação em documentos longos"

# Documentação
git commit -m "docs(readme): adiciona seção de instalação"

# Refatoração
git commit -m "refactor(transpor): simplifica lógica de transposição"

# Com descrição detalhada
git commit -m "feat(mobile): adiciona swipe gesture para menu

Implementa detecção de swipe na borda esquerda da tela.
Quando o usuário arrasta da borda, o menu lateral abre.

Closes #42"
```

---

## 🔀 Pull Requests

### Antes de Abrir um PR

- [ ] Código segue os padrões do projeto
- [ ] Commits seguem o padrão Conventional Commits
- [ ] Código foi testado em múltiplos navegadores
- [ ] Documentação foi atualizada (se necessário)
- [ ] CHANGELOG foi atualizado (se necessário)
- [ ] Não há conflitos com a branch main

### Template de PR

```markdown
## 📋 Descrição

Breve descrição das mudanças.

## 🎯 Tipo de Mudança

- [ ] 🐛 Bug fix
- [ ] ✨ Nova feature
- [ ] 💥 Breaking change
- [ ] 📝 Documentação
- [ ] 🎨 Estilo/UI

## 🧪 Como Testar

1. Vá para o Passo X
2. Faça Y
3. Observe Z

## 📸 Screenshots

(Se aplicável)

## ✅ Checklist

- [ ] Código testado localmente
- [ ] Testado em Chrome, Firefox e Safari
- [ ] Testado em mobile
- [ ] Documentação atualizada
- [ ] CHANGELOG atualizado
- [ ] Commits seguem o padrão

## 🔗 Issues Relacionadas

Closes #123
Relates to #456
```

### Processo de Review

1. **Automated checks** - Verificações automáticas (se configuradas)
2. **Code review** - Revisão por mantenedores
3. **Testing** - Testes adicionais se necessário
4. **Approval** - Aprovação final
5. **Merge** - Merge para a branch principal

---

## 🎨 Diretrizes de Design

### Cores

Use as variáveis CSS definidas:
```css
--cor-primaria: #3b82f6;
--cor-sucesso: #10b981;
--cor-perigo: #ef4444;
--cor-alerta: #f59e0b;
```

### Espaçamento

Use múltiplos de 4px:
```css
padding: 8px;   /* Pequeno */
padding: 12px;  /* Médio */
padding: 16px;  /* Normal */
padding: 24px;  /* Grande */
```

### Tipografia

```css
font-size: 12px;  /* Pequeno */
font-size: 14px;  /* Normal */
font-size: 16px;  /* Médio */
font-size: 18px;  /* Grande */
font-size: 22px;  /* Título */
```

---

## 🧪 Testes

### Checklist de Testes

- [ ] **Desktop**
  - [ ] Chrome (última versão)
  - [ ] Firefox (última versão)
  - [ ] Safari (última versão)
  - [ ] Edge (última versão)

- [ ] **Mobile**
  - [ ] iOS Safari
  - [ ] Android Chrome
  - [ ] Orientação portrait e landscape

- [ ] **Funcionalidades**
  - [ ] Criar seção
  - [ ] Converter cifra
  - [ ] Transpor tom
  - [ ] Salvar projeto
  - [ ] Carregar projeto
  - [ ] Gerar PDF
  - [ ] Modo escuro

---

## 📞 Dúvidas?

Se tiver alguma dúvida sobre como contribuir:

- 💬 Abra uma [Discussion](../../discussions)
- 📧 Envie um email para: contribuir@cifrasstudio.com
- 🐛 Crie uma [Issue](../../issues) com a tag `question`

---

## 🙏 Agradecimentos

Obrigado por contribuir com o Cifras Studio! Sua ajuda é muito apreciada. 🎸

---

<div align="center">

**Feito com ❤️ para a comunidade musical**

</div>
