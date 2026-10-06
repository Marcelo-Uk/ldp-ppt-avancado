# Desafio Extra: Pedra, Papel, Tesoura, Lagarto e Spock

**Lógica de Programação** · para quem já concluiu o desafio anterior

No **mesmo repositório** do desafio anterior, crie a versão **Pedra, Papel, Tesoura, Lagarto e Spock**.

## Regras do jogo

O jogo foi criado por Sam Kass e Karen Bryla e popularizado pela série *The Big Bang Theory*. São **5 jogadas**, e cada uma vence outras 2 e perde para outras 2. Jogadas iguais empatam.

| Jogada | Vence | Perde para |
|---|---|---|
| **Pedra** | tesoura (esmaga), lagarto (esmaga) | papel (cobre), Spock (vaporiza) |
| **Papel** | pedra (cobre), Spock (refuta) | tesoura (corta), lagarto (come) |
| **Tesoura** | papel (corta), lagarto (decapita) | pedra (esmaga), Spock (quebra) |
| **Lagarto** | Spock (envenena), papel (come) | pedra (esmaga), tesoura (decapita) |
| **Spock** | tesoura (quebra), pedra (vaporiza) | lagarto (envenena), papel (refuta) |

## O jogo deve ter

1. Sorteio da jogada do computador a cada rodada, entre as 5 jogadas.
2. Leitura da jogada do jogador (`pedra`, `papel`, `tesoura`, `lagarto` ou `spock`, em minúsculas).
3. Aplicação das 10 regras da tabela acima. Jogadas iguais resultam em empate.
4. Exibição da jogada do computador e do resultado de cada rodada (vitória, derrota ou empate), junto com a **regra que decidiu a rodada** (exemplo: "Lagarto envenena Spock"). No empate não há regra a exibir.
5. Placar atualizado e exibido após cada rodada. Empate não conta ponto.
6. O torneio termina quando alguém fizer **3 vitórias**, com exibição do campeão.
7. Jogada inválida: o programa avisa e pede a jogada novamente, **sem contar como rodada**.
8. A palavra `sair` encerra o jogo a qualquer momento.
9. Ao final do torneio, exibir o total de rodadas jogadas e o total de empates.
10. Histórico das rodadas guardado em uma **lista** e exibido ao final (jogada do jogador, jogada do computador, resultado e regra de cada rodada).
11. Ao final, perguntar se o jogador quer jogar outro torneio. Se sim, tudo volta a zero.

## O que será necessário implementar

- Sorteio com `random.randint(1, 5)` e conversão do número em jogada com `match`/`case`.
- Validação das cinco jogadas permitidas.
- Decisão do resultado: são 5 jogadas x 4 adversários possíveis, ou seja, **20 combinações** que resultam em vitória ou derrota, mais os 5 empates. Cada combinação precisa produzir o resultado e a frase da regra. **Dica:** use um `match` pela jogada do jogador e, dentro de cada `case`, um `if`/`elif` pela jogada do computador.
- Uma variável para guardar a regra da rodada, que será exibida e salva no histórico.
- Atualização do placar a partir do resultado.

## Requisitos técnicos

Utilizar `while`, `if`/`elif`/`else`, `match`/`case`, `random`, lista com `append` e `for`. O código deve ser **comentado**.

## Requisitos de Git

- Usar o **mesmo repositório** do desafio anterior. O novo jogo fica em um arquivo separado, `pedra_papel_tesoura_lagarto_spock.py`, e o arquivo do desafio anterior deve permanecer intacto.
- No mínimo **2 novos commits**, com mensagens que descrevam o que foi feito em cada um.
- Todo o trabalho deve ser enviado ao GitHub com `git push`.

## Entrega

O **mesmo link do repositório**, agora com os dois jogos.
