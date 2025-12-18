# Prompt Master para Geração de Relatórios Interativos HTML

## 📝 Visão Geral

Este é um prompt mestre para criar relatórios interativos e responsivos em HTML + CSS + JavaScript, baseado nos padrões identificados nos relatórios existentes do sistema. O prompt garante consistência visual e funcionalidade mantendo flexibilidade para personalização.

## 🎯 O Que Este Prompt Gera

- **Relatórios HTML completos**: Single-file com CSS e JavaScript embutidos
- **Design responsivo**: Mobile-first approach
- **Interatividade**: Seções expansíveis, modal, animações
- **Visual moderno**: Gradientes, sombras, transições suaves
- **Acessibilidade**: HTML5 semântico, contraste adequado
- **📊 Visualização de dados históricos**: Gráficos interativos, timelines, mapas históricos
- **📈 Análise temporal**: Evolução de eventos e tendências históricas

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

### 3.1. SEÇÃO COM GRÁFICO (NOVO)
```html
<div class="chart-section">
    <h3>[TÍTULO DO GRÁFICO]</h3>
    <div class="chart-container">
        <canvas id="[ID_GRAFICO]" width="400" height="200"></canvas>
    </div>
    <div class="chart-legend">
        <span class="legend-item"><span class="legend-color" style="background: [COR]"></span>[LEGENDA 1]</span>
        <span class="legend-item"><span class="legend-color" style="background: [COR]"></span>[LEGENDA 2]</span>
    </div>
    <p class="chart-description">[ANÁLISE DO GRÁFICO]</p>
</div>
```

### 3.2. TIMELINE HISTÓRICO (NOVO)
```html
<div class="timeline-container">
    <h3>[TÍTULO DA TIMELINE]</h3>
    <div class="timeline">
        <div class="timeline-item">
            <div class="timeline-date">[ANO/PERÍODO]</div>
            <div class="timeline-content">
                <h4>[EVENTO]</h4>
                <p>[DESCRIÇÃO DETALHADA]</p>
                <span class="timeline-impact">[IMPACTO]</span>
            </div>
        </div>
        <!-- Repetir para cada evento -->
    </div>
</div>
```

### 3.3. MAPA HISTÓRICO INTERATIVO (NOVO)
```html
<div class="map-section">
    <h3>[TÍTULO DO MAPA]</h3>
    <div class="map-container">
        <svg id="mapSvg" viewBox="0 0 800 600">
            <!-- Elementos do mapa -->
            <g class="state" onclick="showStateInfo('[ESTADO]')" data-state="[ESTADO]">
                <path d="[PATH_SVG]" fill="[COR]" stroke="#333" stroke-width="1"/>
                <text x="[X]" y="[Y]" text-anchor="middle" fill="#fff">[SIGLA]</text>
            </g>
        </svg>
    </div>
    <div class="map-legend">
        <h4>Legenda:</h4>
        <div class="legend-items">
            <span class="legend-item"><span class="legend-color" style="background: [COR]"></span>[DESCRIÇÃO]</span>
        </div>
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
- `.chart-section` - Container para gráficos
- `.timeline-container` - Container para timeline histórica
- `.timeline-item` - Item individual da timeline
- `.map-section` - Container para mapas interativos
- `.chart-container` - Canvas do gráfico com responsividade
- `.legend-item` - Item da legenda do gráfico
- `.timeline-impact` - Badge de impacto do evento

### Classes para Análise Histórica (NOVO)
```css
.chart-container {
    position: relative;
    height: 300px;
    margin: 20px 0;
}

.timeline {
    position: relative;
    padding: 20px 0;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 50%;
    top: 0;
    bottom: 0;
    width: 2px;
    background: var(--primary-color);
}

.timeline-item {
    position: relative;
    margin-bottom: 30px;
    display: flex;
    align-items: center;
}

.timeline-item:nth-child(odd) {
    flex-direction: row;
}

.timeline-item:nth-child(even) {
    flex-direction: row-reverse;
}

.timeline-date {
    flex: 0 0 120px;
    font-weight: bold;
    color: var(--primary-color);
}

.timeline-content {
    flex: 1;
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: var(--shadow);
    margin: 0 20px;
    position: relative;
}

.timeline-content::before {
    content: '';
    position: absolute;
    width: 20px;
    height: 20px;
    background: var(--accent-color);
    border-radius: 50%;
    top: 50%;
    transform: translateY(-50%);
}

.timeline-item:nth-child(odd) .timeline-content::before {
    left: -30px;
}

.timeline-item:nth-child(even) .timeline-content::before {
    right: -30px;
}

.timeline-impact {
    display: inline-block;
    padding: 4px 8px;
    background: var(--accent-color);
    color: white;
    border-radius: 4px;
    font-size: 12px;
    margin-top: 10px;
}

.map-container {
    text-align: center;
    margin: 20px 0;
}

.map-container svg {
    max-width: 100%;
    height: auto;
}

.state {
    cursor: pointer;
    transition: all 0.3s ease;
}

.state:hover {
    opacity: 0.8;
    transform: scale(1.05);
}

.chart-legend {
    display: flex;
    flex-wrap: wrap;
    gap: 15px;
    margin: 15px 0;
}

.legend-item {
    display: flex;
    align-items: center;
    gap: 8px;
}

.legend-color {
    width: 16px;
    height: 16px;
    border-radius: 4px;
}
```

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

// 7. Renderização de Gráficos (NOVO)
function drawLineChart(canvasId, data, labels) {
    const canvas = document.getElementById(canvasId);
    if (!canvas) return;

    const ctx = canvas.getContext('2d');
    const width = canvas.width;
    const height = canvas.height;

    // Limpa canvas
    ctx.clearRect(0, 0, width, height);

    // Configurações
    const padding = 40;
    const chartWidth = width - 2 * padding;
    const chartHeight = height - 2 * padding;

    // Encontra valores máximos e mínimos
    const maxValue = Math.max(...data.flat());
    const minValue = Math.min(...data.flat());
    const valueRange = maxValue - minValue;

    // Desenha eixos
    ctx.strokeStyle = '#ccc';
    ctx.lineWidth = 1;
    ctx.beginPath();
    ctx.moveTo(padding, padding);
    ctx.lineTo(padding, height - padding);
    ctx.lineTo(width - padding, height - padding);
    ctx.stroke();

    // Desenha linhas de dados
    const colors = ['#e74c3c', '#3498db', '#2ecc71', '#f39c12'];

    data.forEach((dataset, datasetIndex) => {
        ctx.strokeStyle = colors[datasetIndex % colors.length];
        ctx.lineWidth = 2;
        ctx.beginPath();

        dataset.forEach((value, index) => {
            const x = padding + (index / (dataset.length - 1)) * chartWidth;
            const y = height - padding - ((value - minValue) / valueRange) * chartHeight;

            if (index === 0) {
                ctx.moveTo(x, y);
            } else {
                ctx.lineTo(x, y);
            }
        });

        ctx.stroke();

        // Desenha pontos
        dataset.forEach((value, index) => {
            const x = padding + (index / (dataset.length - 1)) * chartWidth;
            const y = height - padding - ((value - minValue) / valueRange) * chartHeight;

            ctx.fillStyle = colors[datasetIndex % colors.length];
            ctx.beginPath();
            ctx.arc(x, y, 4, 0, 2 * Math.PI);
            ctx.fill();
        });
    });

    // Desenha labels
    ctx.fillStyle = '#333';
    ctx.font = '12px Arial';
    ctx.textAlign = 'center';

    if (labels) {
        labels.forEach((label, index) => {
            const x = padding + (index / (labels.length - 1)) * chartWidth;
            ctx.fillText(label, x, height - padding + 20);
        });
    }
}

// 8. Animação de Timeline (NOVO)
function animateTimeline() {
    const timelineItems = document.querySelectorAll('.timeline-item');
    const observer = new IntersectionObserver((entries) => {
        entries.forEach((entry) => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = '1';
                entry.target.style.transform = 'translateY(0)';
            }
        });
    }, { threshold: 0.1 });

    timelineItems.forEach((item, index) => {
        item.style.opacity = '0';
        item.style.transform = 'translateY(20px)';
        item.style.transition = `all 0.5s ease ${index * 0.1}s`;
        observer.observe(item);
    });
}

// 9. Informações do Mapa (NOVO)
function showStateInfo(state) {
    const info = {
        'SP': 'São Paulo: Centro industrial e operário, importante na formação do PCB',
        'RJ': 'Rio de Janeiro: Berço do movimento comunista brasileiro, sede da Revolução de 1935',
        'RS': 'Rio Grande do Sul: Forte influência anarquista e comunista nas áreas rurais',
        'PE': 'Pernambuco: Destaque nas Ligas Camponesas e movimento comunista rural',
        'PA': 'Pará: Importante na Guerrilha do Araguaia',
        'GO': 'Goiás: Palco da Guerrilha do Araguaia'
    };

    const message = info[state] || `${state}: Participação ativa no movimento comunista brasileiro`;

    // Cria tooltip ou modal
    const tooltip = document.createElement('div');
    tooltip.className = 'map-tooltip';
    tooltip.innerHTML = `<strong>${state}</strong><br>${message}`;
    tooltip.style.cssText = `
        position: fixed;
        background: white;
        padding: 15px;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.2);
        z-index: 1000;
        max-width: 250px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    `;

    document.body.appendChild(tooltip);

    setTimeout(() => {
        tooltip.remove();
    }, 3000);
}

// 10. Inicialização Extendida (ATUALIZADO)
document.addEventListener('DOMContentLoaded', function() {
    // Anima números ao carregar
    animateNumbers();

    // Anima timeline
    animateTimeline();

    // Desenha gráficos
    if (typeof chartData !== 'undefined') {
        chartData.forEach(chart => {
            drawLineChart(chart.id, chart.data, chart.labels);
        });
    }

    // Abre primeira seção automaticamente
    const firstSection = document.querySelector('.section-header');
    if (firstSection) {
        toggleSection(firstSection);
    }

    // Adiciona filtros para timeline
    addTimelineFilters();
});

// 11. Filtros de Timeline (NOVO)
function addTimelineFilters() {
    const filterContainer = document.createElement('div');
    filterContainer.className = 'timeline-filters';
    filterContainer.innerHTML = `
        <button onclick="filterTimeline('all')">Todos</button>
        <button onclick="filterTimeline('political')">Político</button>
        <button onclick="filterTimeline('social')">Social</button>
        <button onclick="filterTimeline('militar')">Militar</button>
    `;

    const timeline = document.querySelector('.timeline-container');
    if (timeline) {
        timeline.insertBefore(filterContainer, timeline.firstChild);
    }
}

function filterTimeline(type) {
    const items = document.querySelectorAll('.timeline-item');
    items.forEach(item => {
        if (type === 'all' || item.dataset.category === type) {
            item.style.display = 'flex';
        } else {
            item.style.display = 'none';
        }
    });

    // Atualiza botões
    document.querySelectorAll('.timeline-filters button').forEach(btn => {
        btn.classList.remove('active');
    });
    event.target.classList.add('active');
}
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

### Exemplo 3: Comunismo no Brasil (NOVO)
```
Tema: Contexto Histórico do Comunismo no Brasil (1922-2024)
Público: Estudantes de história, pesquisadores e interessados em política
Tipo: Histórico/Acadêmico

Paleta de Cores:
- Cor Primária: Vermelho #e74c3c (simbolismo comunista)
- Cor Secundária: Azul escuro #2c3e50 (seriedade histórica)
- Cor de Destaque: Dourado #f39c12 (resistência e esperança)

Elementos Específicos:
- Timeline de eventos políticos (1922-2024)
- Gráfico de evolução da militância comunista
- Mapa do Brasil com focos de resistência
- Perfil biográfico de líderes comunistas
- Análise de políticas de repressão
- Comparação entre diferentes períodos históricos
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

### Histórico/Político (NOVO)
- **Comunismo/Socialismo**: Vermelho #e74c3c + Azul escuro #2c3e50 + Dourado #f39c12
- **Democracia**: Verde #27ae60 + Azul #3498db + Branco #ecf0f1
- **Ditadura/Militar**: Cinza escuro #34495e + Vermelho escuro #c0392b + Preto #2c3e50
- **Resistência**: Laranja #e67e22 + Amarelo #f1c40f + Verde #2ecc71

### Cores Históricas Brasileiras (NOVO)
- **Período Imperial**: Verde #009739 + Amarelo #fedd00 + Azul #012169
- **Era Vargas**: Vermelho #c1272d + Preto #000000 + Branco #ffffff
- **Ditadura Militar**: Verde oliva #556b2f + Marrom #8b4513 + Cinza #708090
- **Redemocratização**: Azul #4169e1 + Verde #228b22 + Amarelo #ffd700

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
- [ ] Gráficos e visualizações funcionando corretamente
- [ ] Timeline animada e responsiva
- [ ] Mapa interativo com informações corretas

## 🚀 Próximos Passos

1. **Teste local**: Salve o HTML gerado e abra no navegador
2. **Valide o código**: Use validadores HTML/CSS
3. **Teste responsividade**: Chrome DevTools - Device Mode
4. **Verifique acessibilidade**: WAVE ou Lighthouse
5. **Otimize**: Comprima imagens, minifique se necessário
6. **Deploy**: Hospede em servidor web estático
7. **Teste visualizações**: Verifique gráficos, timelines e mapas
8. **Valide dados**: Confira precisão histórica e estatística

## 📚 Recursos Adicionais

- [HTML5 Semantic Elements](https://developer.mozilla.org/en-US/docs/Glossary/Semantic_HTML)
- [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)
- [Web Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [Responsive Design Patterns](https://web.dev/responsive-web-design-basics/)
- [Canvas API for Charts](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
- [SVG for Interactive Maps](https://developer.mozilla.org/en-US/docs/Web/SVG)
- [Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API)

## 📖 Conteúdo Específico: Comunismo no Brasil (Exemplo Completo)

### Título: "Século Vermelho: A Trajetória do Comunismo no Brasil (1922-2024)"

#### Contexto Histórico:
- Fundação do Partido Comunista Brasileiro (PCB) em 1922
- Influência da Revolução Russa e do movimento operário
- Períodos de legalidade e clandestinidade
- Relação com outros movimentos sociais e políticos

#### Estatísticas Essenciais:
1. **1922** - Ano de fundação do PCB
2. **1935** - Ano da Intentona Comunista
3. **1964-1985** - Período de maior repressão (Ditadura Militar)
4. **~400.000** - Estimativa de militantes em momentos de pico
5. **2.300** - Número aproximado de mortos e desaparecidos políticos
6. **8** - Número de partidos com origem comunista/ socialista hoje

#### Timeline Principal:
1. **1922-1935**: Formação e primeiros anos do PCB
2. **1935-1945**: Repressão varguista e participação na resistência
3. **1945-1964**: Breve legalidade e atuação institucional
4. **1964-1979**: Clandestinidade e resistência armada
5. **1979-1985**: Anistia e redemocratização
6. **1985-2024**: Transição para partidos legais e atuação democrática

#### Focos de Resistência (Mapa):
- **Sudeste**: SP, RJ, MG - Centros industriais e operários
- **Nordeste**: PE, PB, CE - Ligas Camponesas e movimento rural
- **Norte**: PA, AM, GO - Guerrilha do Araguaia
- **Sul**: RS, SC - Influência anarquista e imigrante

#### Gráficos Sugeridos:
- Evolução da militância (1922-2024)
- Comparativo: Repressão vs. Organização
- Distribuição geográfica por décadas
- Relação com outros movimentos sociais

---

**Nota**: Este prompt foi criado baseado na análise dos relatórios existentes do sistema, garantindo consistência e qualidade em todas as gerações futuras. A versão adaptada inclui recursos específicos para análise histórica e visualização de dados temporais.