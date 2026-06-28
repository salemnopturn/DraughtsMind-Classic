# ⛃ DraughtsMind Classic ⛃

> **Think Deeper. Play Better.**

Motor de IA de alto desempenho para **Damas Brasileiras** (regras CBD), rodando 100% no navegador — sem instalação, sem servidor, sem internet.

---

## 🎮 Demo

Basta abrir o arquivo `DraughtsMind Classic.html` no navegador. Nenhuma instalação necessária.

---

## ✨ Funcionalidades

- **Motor reengenheirado** — Zobrist 64-bit BigInt, Tabela de Transposição compacta 262K (2-way `Uint32Array`), algoritmos PVS + LMR + NMP + IID + qsearch
- **Avaliação posicional** — PST (Piece-Square Tables), controle do centro e penalização de bordas
- **Board Editor embutido** — edite posições livremente antes de jogar
- **Livro de Aberturas Master** — mais de 3.100 linhas maximais
- **Fidelidade às regras CBD** — Lei da Maioria, tripla repetição, regra dos 20 lances, finais Art. 59/100
- **PDN import/export** — compatível com o formato padrão de Damas
- **Análise em tempo real** — avaliação e profundidade exibidas durante o jogo
- **Árvore de variantes** — explore linhas alternativas
- **100% offline** — nenhuma chamada de rede, nenhum dado enviado a servidores

---

## 🚀 Como usar

1. Faça o download do arquivo `DraughtsMind Classic.html`
2. Abra-o em qualquer navegador moderno (Chrome, Firefox, Edge, Safari)
3. Jogue!

Não é necessário instalar nada, criar conta ou ter conexão com a internet.

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

---

## 🧠 Sobre o Motor

O DraughtsMind utiliza técnicas avançadas de busca em jogos:

- **PVS** (Principal Variation Search) — variante otimizada do alpha-beta
- **LMR** (Late Move Reductions) — redução de profundidade para lances tardios
- **NMP** (Null Move Pruning) — poda por lance nulo
- **IID** (Internal Iterative Deepening) — aprofundamento iterativo interno
- **Qsearch** — busca de quiescência para evitar o efeito horizonte
- **Zobrist Hashing 64-bit** com `BigInt` para detecção de repetição e TT
- **Livro de aberturas** integrado com +3.100 posições

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
