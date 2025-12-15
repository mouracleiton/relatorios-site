# Prompt Master para Geração de Relatórios Interativos HTML

## 📝 Visão Geral

Este é um prompt mestre para criar relatórios interativos e responsivos em HTML + CSS + JavaScript, baseado nos padrões identificados nos relatórios existentes do sistema. O prompt garante consistência visual e funcionalidade mantendo flexibilidade para personalização.

## 🎯 O Que Este Prompt Gera

- **Relatórios HTML completos**: Single-file com CSS e JavaScript embutidos
- **Design responsivo**: Mobile-first approach
- **Interatividade**: Seções expansíveis, modal, animações
- **Visual moderno**: Gradientes, sombras, transições suaves
- **Acessibilidade**: HTML5 semântico, contraste adequado

## 🚀 Como Usar

### Passo 1: Copie o prompt completo
Copie todo o conteúdo do prompt master fornecido abaixo

### Passo 2: Personalize os campos
Preencha todos os campos entre colchetes `[ ]` com suas informações específicas:

#### Configurações Básicas
```
Tema: [ESPECIFICAR O TEMA]
Público-alvo: [DEFINIR PÚBLICO]
Tipo: [Acadêmico/Empresarial/Técnico/Social]
```

#### Paleta de Cores
```
- Cor Primária: [Cor principal] - usar em headers e elementos principais
- Cor Secundária: [Cor secundária] - usar em sections e cards
- Cor de Destaque: [Cor de destaque] - usar em elementos especiais e hover effects
```

#### Conteúdo Específico
- **Título completo**: Nome do relatório
- **Contexto**: Descrição do cenário
- **Estatísticas**: 4-6 números principais
- **Seções**: Tópicos do conteúdo
- **Políticas**: Iniciativas por nível governamental
- **Fases**: Etapas de implementação
- **Resumo Executivo**: Pontos-chave em bullets

### Passo 3: Execute o prompt
Cole o prompt personalizado em sua IA de preferência (Claude, ChatGPT, etc.) e execute.

## 📄 O Prompt Master

```html
Você é um especialista em criar relatórios interativos em HTML + CSS + JavaScript. Crie um relatório completo e visualmente atraente seguindo todas as especificações abaixo:

## 📋 ESTRUTURA DO RELATÓRIO

### Tema: [ESPECIFICAR O TEMA]
Público-alvo: [DEFINIR PÚBLICO]
Tipo: [Acadêmico/Empresarial/Técnico/Social]

## 🎨 PALETA DE CORES

Defina uma paleta de cores coerente com o tema:
- **Cor Primária**: [Cor principal] - usar em headers e elementos principais
- **Cor Secundária**: [Cor secundária] - usar em sections e cards
- **Cor de Destaque**: [Cor de destaque] - usar em elementos especiais e hover effects

## 📊 SEÇÕES OBRIGATÓRIAS

### 1. HEADER
```html
<header>
    <div class="header-content">
        <span class="emoji">[EMOJI DO TEMA]</span>
        <h1>[TÍTULO PRINCIPAL]</h1>
        <p>[Subtítulo descritivo]</p>
    </div>
</header>
```

### 2. GRID DE ESTATÍSTICAS (4-6 cartões)
```html
<section class="stats-grid">
    <div class="stat-card">
        <div class="stat-number">[NÚMERO COM FORMATAÇÃO]</div>
        <div class="stat-label">[DESCRIÇÃO]</div>
        <div class="stat-indicator">[SETAS/MÉTRICA]</div>
    </div>
    <!-- Repetir para cada estatística -->
</section>
```

### 3. SEÇÃO PRINCIPAL
```html
<div class="section active">
    <div class="section-header" onclick="toggleSection(this)">
        <span class="emoji">[EMOJI]</span>
        <h2>[TÍTULO DA SEÇÃO]</h2>
        <span class="expand-arrow">▼</span>
    </div>
    <div class="section-content">
        [CONTEÚDO DETALHADO]
    </div>
</div>
```

### 4. GRID DE POLÍTICAS/DESAFIOS/OPORTUNIDADES
```html
<div class="policy-grid">
    <div class="policy-card">
        <div class="policy-icon">🏛️</div>
        <h3>Nível Federal</h3>
        [Conteúdo específico]
    </div>
    <!-- Repetir para outros níveis -->
</div>
```

### 5. GRID DE FASES/KPIs/PERFIS
```html
<div class="implementation-phases">
    <div class="phase-card">
        <div class="phase-number">1</div>
        <h3>[Título da Fase]</h3>
        <ul>[Lista de atividades]</ul>
    </div>
    <!-- Repetir para cada fase -->
</div>
```

### 6. FOOTER
```html
<footer>
    <p>&copy; 2024 [Organização]. Todos os direitos reservados.</p>
    <p>Fonte: [Referências]</p>
</footer>
```

### 7. BOTÃO FOTUANTE E MODAL
```html
<button class="floating-button" onclick="openSummary()">📋</button>

<div class="modal" id="summaryModal">
    <div class="modal-content">
        <span class="close" onclick="closeSummary()">&times;</span>
        <h2>Resumo Executivo</h2>
        <div class="summary-content">
            [Resumo completo em bullets]
        </div>
    </div>
</div>
```

## 🎯 REGRAS DE CSS

### Variáveis CSS (obrigatório)
```css
:root {
    --primary-color: #[COR_HEX];
    --dark-primary: #[COR_ESCURA];
    --secondary-color: #[COR_HEX];
    --dark-secondary: #[COR_ESCURA];
    --accent-color: #[COR_HEX];
    --dark-accent: #[COR_ESCURA];
    --shadow: 0 2px 10px rgba(0,0,0,0.1);
    --shadow-hover: 0 5px 20px rgba(0,0,0,0.15);
}
```

### Gradientes Padrão
```css
body {
    background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
}

header {
    background: linear-gradient(135deg, var(--primary-color), var(--dark-primary));
}

.section-header {
    background: linear-gradient(135deg, var(--secondary-color), var(--dark-secondary));
}
```

### Classes Essenciais
- `.container` - Container principal max-width 1200px
- `.stats-grid` - Grid 3-4 colunas responsive
- `.section` - Seção expansível com accordion
- `.section-content` - Conteúdo animado com fadeIn
- `.modal` - Modal overlay
- `.floating-button` - Botão circular fixo

## ⚡ FUNCIONALIDADES JAVASCRIPT OBRIGATÓRIAS

```javascript
// 1. Toggle de Seções (Accordion)
function toggleSection(header) {
    const content = header.nextElementSibling;
    const allSections = document.querySelectorAll('.section');
    const allHeaders = document.querySelectorAll('.section-header');

    // Fecha outras seções
    allSections.forEach(section => {
        if (section !== header.parentElement) {
            section.classList.remove('active');
        }
    });

    allHeaders.forEach(h => {
        if (h !== header) {
            h.classList.remove('active');
        }
    });

    // Abre/fecha seção atual
    header.parentElement.classList.toggle('active');
    header.classList.toggle('active');
}

// 2. Animação de Números
function animateNumbers() {
    const numbers = document.querySelectorAll('.stat-number');
    numbers.forEach(num => {
        const target = parseFloat(num.innerText.replace(/[^0-9.-]/g, ''));
        const increment = target / 50;
        let current = 0;

        const updateNumber = () => {
            current += increment;
            if (current < target) {
                num.innerText = formatNumber(current);
                requestAnimationFrame(updateNumber);
            } else {
                num.innerText = num.innerText; // Mantém formatação original
            }
        };

        updateNumber();
    });
}

// 3. Controle do Modal
function openSummary() {
    document.getElementById('summaryModal').style.display = 'flex';
    document.body.style.overflow = 'hidden';
}

function closeSummary() {
    document.getElementById('summaryModal').style.display = 'none';
    document.body.style.overflow = 'auto';
}

// 4. Inicialização
document.addEventListener('DOMContentLoaded', function() {
    // Anima números ao carregar
    animateNumbers();

    // Abre primeira seção automaticamente
    const firstSection = document.querySelector('.section-header');
    if (firstSection) {
        toggleSection(firstSection);
    }
});

// 5. Fecha modal clicando fora
window.onclick = function(event) {
    const modal = document.getElementById('summaryModal');
    if (event.target == modal) {
        closeSummary();
    }
}

// 6. Smooth scroll para âncoras
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        if (target) {
            target.scrollIntoView({ behavior: 'smooth' });
        }
    });
});
```

## 📝 CONTEÚDO ESPECÍFICO [Personalizar aqui]

### Título: [TÍTULO COMPLETO]
- **Contexto**: [Descrição do contexto]
- **Dados Principais**: [Lista de estatísticas-chave]
- **Público**: [Descrição do público-alvo]
- **Objetivo**: [Objetivo do relatório]

### Estatísticas Essenciais:
1. [Valor 1] - [Descrição completa]
2. [Valor 2] - [Descrição completa]
3. [Valor 3] - [Descrição completa]
4. [Valor 4] - [Descrição completa]
5. [Valor 5] - [Descrição completa]
6. [Valor 6] - [Descrição completa]

### Seções Principais:
1. **[Título Seção 1]** - [Breve descrição]
2. **[Título Seção 2]** - [Breve descrição]
3. **[Título Seção 3]** - [Breve descrição]
4. **[Título Seção 4]** - [Breve descrição]
5. **[Título Seção 5]** - [Breve descrição]

### Políticas/Iniciativas:
- **Federal**: [Políticas nível federal]
- **Estadual**: [Políticas estaduais]
- **Municipal**: [Políticas locais]

### Fases/Implementação:
1. **[Fase 1]**: [Descrição e atividades]
2. **[Fase 2]**: [Descrição e atividades]
3. **[Fase 3]**: [Descrição e atividades]
4. **[Fase 4]**: [Descrição e atividades]

### Resumo Executivo:
- [Bullet point 1]
- [Bullet point 2]
- [Bullet point 3]
- [Bullet point 4]
- [Bullet point 5]

## ✅ REQUISITOS FINAIS

1. **HTML5 Semântico**: Usar tags header, section, footer, etc.
2. **CSS Mobile-First**: Responsive design breakpoints:
   - Mobile: < 768px
   - Tablet: 768px - 1024px
   - Desktop: > 1024px
3. **Acessibilidade**: Alt text em imagens, contrast ratio adequado
4. **Performance**: Código otimizado, sem dependências externas
5. **Validação**: HTML e CSS válidos
6. **Cross-browser**: Funcional em Chrome, Firefox, Safari, Edge
```

## 💡 Exemplos de Uso

### Exemplo 1: Relatório de Sustentabilidade
```
Tema: Sustentabilidade na Indústria da Moda
Público: Gestores de produção e CEOs
Tipo: Empresarial/Técnico

Paleta de Cores:
- Cor Primária: Verde #2ecc71 (sustentabilidade)
- Cor Secundária: Azul #3498db (indústria)
- Cor de Destaque: Laranja #e67e22 (ação)
```

### Exemplo 2: Relatório Acadêmico
```
Tema: Impacto da IA na Educação Superior
Público: Coordenadores de cursos e diretores
Tipo: Acadêmico/Técnico

Paleta de Cores:
- Cor Primária: Roxo #9b59b6 (inovação)
- Cor Secundária: Azul #2980b9 (educação)
- Cor de Destaque: Amarelo #f39c12 (tecnologia)
```

## 🎨 Paletas de Cores Sugeridas

### Empresarial
- Azul corporativo + cinza + laranja
- Verde profissional + azul marinho + dourado

### Social/ONG
- Verde esperança + azul claro + amarelo
- Laranja vibrante + teal + rosa

### Tecnologia
- Roxo inovação + azul digital + ciano
- Preto elegante + verde matrix + azul neon

### Educação
- Azul conhecimento + verde crescimento + laranja criatividade
- Vermelho paixão + azul lógico + amarelo iluminação

## 📋 Checklist de Validação

Antes de finalizar seu relatório, verifique:

- [ ] HTML5 semântico completo
- [ ] CSS com variáveis customizadas
- [ ] JavaScript funcional sem erros
- [ ] Design responsivo testado
- [ ] Acessibilidade verificada
- [ ] Performance otimizada
- [ ] Cross-browser compatível
- [ ] Conteúdo coeso e bem estruturado
- [ ] Coerência visual mantida

## 🚀 Próximos Passos

1. **Teste local**: Salve o HTML gerado e abra no navegador
2. **Valide o código**: Use validadores HTML/CSS
3. **Teste responsividade**: Chrome DevTools - Device Mode
4. **Verifique acessibilidade**: WAVE ou Lighthouse
5. **Otimize**: Comprima imagens, minifique se necessário
6. **Deploy**: Hospede em servidor web estático

## 📚 Recursos Adicionais

- [HTML5 Semantic Elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantic_HTML)
- [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [Responsive Design Patterns](https://web.dev/responsive-web-design-basics/)

---

**Nota**: Este prompt foi criado baseado na análise dos relatórios existentes do sistema, garantindo consistência e qualidade em todas as gerações futuras.