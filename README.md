# ⛃ DraughtsMind Classic ⛃

> **Think Deeper. Play Better.**

Motor de IA de alto desempenho para **Damas Brasileiras** (regras CBD), rodando 100% no navegador — sem instalação, sem servidor, sem internet.

---

## 🎮 Como usar

Basta abrir o arquivo `DraughtsMind Classic.html` em qualquer navegador moderno. Nenhuma instalação necessária.

---

## ✨ Funcionalidades

### Modos de Jogo

- **Humano vs Humano** — dois jogadores na mesma tela
- **Humano (Brancas) vs CPU (Vermelhas)** — padrão
- **CPU (Brancas) vs Humano (Vermelhas)** — jogue com as vermelhas
- **CPU vs CPU** — observe duas IAs jogando entre si
- **Sandbox (Livre)** — modo livre para experimentos, sem regras de turno

### Níveis de Dificuldade

| Nível | Profundidade | Perfil |
|---|---|---|
| Rápido | Ply 4 | Partidas ágeis |
| Normal | Ply 6 | Uso geral |
| Difícil | Ply 8 | Desafiador |
| Pro | Ply 10 | Padrão recomendado |
| Mestre | Ply 12 | Alto nível |
| Elite | Ply 14 | Para experientes |
| Grandmaster | Ply 16 | Nível máximo |

### Controle de Tempo

| Formato | Tempo |
|---|---|
| Sem Limite | — |
| Bullet | 1 minuto |
| Blitz | 3 ou 5 minutos |
| Rápido | 10 ou 15 minutos |
| Clássico | 30 minutos |
| Pro | 60 minutos |

---

## 🧠 Motor de IA

O DraughtsMind Classic utiliza técnicas avançadas de busca em jogos:

- **PVS** (Principal Variation Search) — variante otimizada do alpha-beta
- **LMR** (Late Move Reductions) — redução de profundidade para lances tardios
- **NMP** (Null Move Pruning) — poda por lance nulo
- **IID** (Internal Iterative Deepening) — aprofundamento iterativo interno
- **Qsearch** — busca de quiescência para evitar o efeito horizonte
- **Zobrist Hashing 64-bit** com `BigInt` para detecção de repetição
- **Tabela de Transposição compacta** de 262K entradas (2-way `Uint32Array`)
- **Avaliação posicional** com PST (Piece-Square Tables), controle do centro e penalização de bordas
- **Livro de Aberturas Master** com mais de 3.100 linhas maximais validadas pelo motor

---

## 📋 Regras e Fidelidade CBD

O motor implementa fielmente as regras da Confederação Brasileira de Damas:

- **Lei da Maioria** — obrigatoriedade de capturar o maior número possível de peças
- **Promoção a Dama** — somente ao final do lance de captura (Art. 13)
- **Tripla repetição** — empate por repetição de posição
- **Regra dos 20 lances** — empate em finais de damas sem captura ou avanço de pedra
- **Art. 59 (finais de damas):**
  - `1D × 1D` — empate em 2 lances
  - Finais com `1D+1P × 1D` e variantes — empate em 5 lances
- **Art. 100** — finais específicos com dama solitária na grande diagonal

---

## 🛠️ Ferramentas de Análise e Edição

### Análise em Tempo Real
- Avaliação da posição em centipedões
- Profundidade de busca atual
- Tempo de cálculo
- Indicação de jogada do livro de aberturas com `[📖 Livro]`

### Botão Sugestão
- Calcula e exibe a melhor jogada disponível para o jogador atual
- Indica a avaliação e profundidade da busca realizada
- Destaca visualmente a peça e os destinos sugeridos

### Botão Forçar Engine
- Força a CPU a jogar imediatamente, mesmo fora do turno configurado

### Board Editor (Editor de Posição)
- Ative com o botão **Editar**
- Clique com o **botão esquerdo** para adicionar peças (pedras e damas, brancas ou vermelhas)
- Clique com o **botão direito** para remover peças
- Escolha de quem é o turno inicial (Brancas ou Vermelhas)
- Ao iniciar, o jogo continua a partir da posição editada

### Contador de Peças
- Exibe em tempo real o número de pedras (`P`) e damas (`D`) de cada lado

### Estatísticas da CPU (CPU vs CPU)
- Placar de vitórias, empates e derrotas por partida no modo CPU vs CPU

---

## 📖 Histórico e Navegação

- **Histórico de lances** exibido em notação algébrica/numérica
- **Árvore de variantes** — explore linhas alternativas diretamente no tabuleiro
- **Modal de escolha** ao realizar um lance em posição já existente: substituir ou adicionar variação
- Navegação por botões e atalhos de teclado:

| Ação | Botão | Teclado |
|---|---|---|
| Ir ao início | `\|<` | ↑ |
| Lance anterior | `<` | ← |
| Próximo lance | `>` | → |
| Ir ao fim | `>\|` | ↓ |

---

## 💾 Importação e Exportação PDN

- **Exportar** — salva a partida atual (incluindo variantes) no formato `.pdn` padrão
- **Importar** — carrega um arquivo `.pdn` existente 
- **Colar PDN** — cole uma sequência de lances diretamente na caixa de texto e clique em **Validar & Reconstruir**

O PDN exportado inclui metadados como versão do motor, profundidade, tempo e hash da posição.

---

## 🖥️ Compatibilidade

| Sistema Operacional | Suporte |
|---|---|
| Windows | ✅ |
| macOS | ✅ |
| Linux | ✅ |

Requer um navegador moderno com suporte a **BigInt** e **ES2020+** (Chrome 67+, Firefox 68+, Safari 14+, Edge 79+).

---

## 🔒 Privacidade e Segurança

- Nenhuma conexão com servidores externos
- Nenhum dado coletado ou transmitido
- Nenhum rastreador, cookie ou anúncio
- Código totalmente auditável — um único arquivo HTML autocontido
- 100% offline: funciona sem internet após o download

---

## 📄 Licença

Distribuído sob a licença **GNU General Public License v3.0 ou posterior**.

Você é livre para usar, estudar, modificar e redistribuir este software, desde que mantenha a mesma licença. Veja o arquivo [LICENSE](LICENSE) para detalhes.

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou pull requests.

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/minha-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona minha feature'`)
4. Push para a branch (`git push origin feature/minha-feature`)
5. Abra um Pull Request

---

<p align="center">⛃ <strong>DraughtsMind Classic</strong> — Think Deeper. Play Better.</p>
