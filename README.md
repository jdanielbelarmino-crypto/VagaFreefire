# Vagalume Multiplayer (Node.js)

Servidor Node.js + Socket.IO para salas multiplayer do jogo Vagalume (até 5 jogadores), pronto para o Render.

## Novidades da versão 1.9

- **História reescrita, com enredo de verdade (modo história solo):** agora existe um fio condutor. A Rainha Noturna não apagou as estrelas por maldade: a primeira delas, **Alba**, caiu nos braços dela, e o medo de perder outra a fez esconder o céu inteiro. Cada um dos 9 personagens do caminho (Cora, Tobias, Ilma, Davi, Yara, Orion, Amun, Cristal e Brasa) guarda **um verso da canção de ninar** da Rainha e tem ligação pessoal com o chefe da noite (o rei amigo do pescador, o cavaleiro que nunca foi dispensado, a mãe de Davi virada corvo, o lobo de Yara, o faraó de Amun...). Na noite 9 o herói descobre que a própria luz que carrega é uma faísca de Alba, e na noite 10 a Rainha a reconhece. O epílogo fecha a canção. Os diálogos funcionam para qualquer um dos 12 heróis, e a fala de cada herói continua entrando em cada capítulo.
- **Frases de início de noite** (as 10) reescritas para combinar com a nova história.
- **Dificuldade mais amena no começo (solo):** os monstros comuns e os chefes das noites 1 a 9 nascem mais fracos e em menor quantidade, e vão aumentando aos poucos ao longo de cada noite, até um nível ainda abaixo do anterior. O **chefão final (Imperador Estelar) não mudou**.
  - Vida inicial do herói +16 no solo.
  - Monstros comuns: começam com ~70% da vida, ~62% do dano e ~45% do ritmo de nascimento, e sobem até ~92%, ~88% e ~85% (em 150 a 220 s).
  - Chefes das noites 1 a 9: -15% de vida e -20% de dano.
  - Mais tempo de invulnerabilidade depois de levar dano (0,95 s) e o dobro de cura caindo dos monstros.
  - Os primeiros níveis exigem menos XP.
- O multiplayer **não mudou** (`server.js` igual ao da 1.8, e os ajustes de dificuldade valem só no solo).

## Novidades da versão 1.8

- **10 monstros novos de combate, um por ambiente**, com visual e comportamento próprios, iguais para todos no multiplayer: Mariposa Sombria (Floresta), Cogumelo Tóxico (Pântano), Coveiro (Cemitério, invoca esqueletos), Abóbora Maldita (Aldeia, investida), Fada do Gelo (Bosque, leque de estilhaços), Fenda Viva (Abismo, anel de projéteis), Gênio das Areias (Dunas, tornados de poeira), Estilhaço Vivo (Caverna, investida), Salamandra (Vulcão, bolas de fogo) e Sentinela Estelar (Cidadela). Entram na rotina de cada noite depois de alguns segundos, em quantidade pequena.

## Novidades da versão 1.7

- **Cinema do modo história (solo):** cada uma das 10 noites abre com uma cena em tela cheia, com cenário próprio, personagem novo do ambiente (Cora, Tobias, Ilma, Davi, Yara, Orion, Amun, Cristal, Brasa e a Rainha Noturna), falas com digitação, lembranças em sépia, chegada dos monstros da noite e aparição do chefe. Toque, Espaço ou Enter avançam; Esc ou "Pular" encerra. A fala do herói escolhido entra em cada capítulo. Epílogo com a Rainha ao vencer a noite 10.
- **Músicas originais:** canção de ninar para as cenas e um tema próprio para 7 das 10 noites (Pântano, Aldeia, Bosque gelado, Dunas, Cristais, Vulcão e Cidadela). Floresta, Cemitério e Abismo mantêm as peças clássicas.
- **Roupas e cabelo animados:** mechas de cabelo e barra da capa reagem ao movimento de todos os heróis.
- **Monstros mais vivos:** balanço, inclinação e respiração; voadores e chefes deixam rastro.
- **Cada chefe com entrada própria** (faixa com o nome, anéis, explosões e som diferentes) e aura própria durante a luta.
- O multiplayer não mudou (`server.js` igual ao da 1.6).

## Novidades da versão 1.6

- **Modo história completo (solo):** agora são **10 capítulos**, um por noite, alinhados aos cenários (antes eram 6 e vários não combinavam com a noite). Cada cena aparece em tela cheia **uma só vez por noite**, com a fala do herói escolhido.
- **A cena também aparece ao avançar de noite dentro da campanha** (antes só aparecia ao iniciar pelo menu). O mundo fica parado durante a cena.
- **Frases de início de noite** (as 10) combinam com o cenário. O **epílogo** só aparece ao vencer a noite 10 no solo.
- **Modo ao vivo revisado:** XP, ouro e curas somem para todos quando um jogador pega, reviver aliado e troca de host no meio da partida foram testados com dois clientes contra o `server.js` real.

## Novidades da versão 1.5

- **Modo história (solo):** cena em tela cheia antes de cada noite (uma só vez por noite), com a fala do herói escolhido, e epílogo ao vencer a noite 10.
- **Equipamento por herói:** 5 níveis, +4% de dano cada, custo crescente em ouro (350, 595, 1011, 1719, 2922), na aba Heróis.
- **Entrada animada de cada chefe** (ondas de energia e tremor) e lenço ao vento em todos os heróis.

## Novidades da versão 1.4

- **Só o líder da sala inicia a partida** (o primeiro a entrar); os outros aguardam e entram quando ele começar. O servidor também bloqueia isso.
- **Heróis não se repetem na sala:** herói em uso fica desabilitado; se dois escolherem ao mesmo tempo, o servidor troca o segundo para um herói livre.
- **Noite seguinte só libera ao vencer a noite atual** (removido o desbloqueio por metade do tempo).
- **XP, ouro e curas somem para todos quando um jogador pega.**
- **Menos monstros na tela** (limite e ritmo de nascimento menores, grupos menores) e **noites mais curtas** (2:30 a 8:30).
- **Chefes mais fortes** e **chefão final**: ao zerar o tempo ele renasce com animação, fica invulnerável por 3 s e precisa ser derrotado para vencer.
- **XP controlado:** gemas valem menos, o nível exige mais XP e há menos gemas acumuladas.
- **Nerf geral de dano (-12%)** e **balanço diário ao vivo:** todo dia alguns heróis ficam +10% ou -10% (aparece no painel do herói).
- **Evento diário** (Lua de sangue, Chuva de estrelas, Névoa densa, Noite calma, Fúria da floresta), igual para todos no mesmo dia.
- **História por noite:** uma frase de história aparece ao iniciar cada noite.

## Novidades da versão 1.3 — heróis totalmente diferentes

Cada um dos 12 heróis agora tem **corpo, animação, Impulso e passiva próprios**:

| Herói | Visual e animação | Impulso (Espaço/Shift) | Passiva |
|---|---|---|---|
| Vaga | pequena, lanterna gigante numa vara que balança e avança ao atacar | Rastro de luz: poças de luz que queimam | Luz viva: luz 22% maior que queima de leve quem chega perto |
| Lia | alta e esguia, capa longa ao vento, puxa a corda do arco | Salto da águia: pula e solta 3 flechas | +12% crítico, mais veloz, flechas atravessam +1, menos vida |
| Bento | largo e pesado, passo de armadura, escudo-torre | Investida de escudo: imune, empurra e atordoa | +30 vida, 16% menos dano, contra-ataque ao ser ferido, mais lento |
| Mara | flutua num vestido longo com pétalas de luz | Passo da aurora: teletransporte que deixa chão de cura | Regenera, cura aliados, ímã maior, menos vida |
| Pipa | redonda e baixinha, mochila de bombas faiscando | Salto-foguete: bombas na saída e na chegada | Estopim: 13% dos abates explodem |
| Tito | agachado e furtivo, poncho e chapéu largo | Rolamento: deixa armadilhas | +10% velocidade, +20% ouro, mais armadilhas |
| Íris | flutua sem pernas, cauda de névoa, lobinho ao lado | Passo espectral: atravessa e solta vagalumes | Lobinho espiritual que caça e morde sozinho |
| Ravi | monge de túnica larga, contas girando, faíscas nas mãos | Relâmpago: teletransporte em raio que fere o caminho | Carga estática: a cada 7 abates cai um raio |
| Nina | pequena, mochila com antena, braço mecânico e drone | Propulsor: voa e deixa uma torreta | +1 torreta, duram mais, menos vida |
| Dom | o mais alto, ombreiras pontudas, capa, auréola e martelo | Investida sagrada: imune, termina em explosão | +10% dano, +15 vida, cura com abates, mais lento |
| Kael | esguio, cachecol longo, imagens residuais ao correr | Corte-relâmpago: corta tudo no caminho, recarga mínima | Ritmo de batalha: ataque rápido, abates recarregam o Impulso |
| Sol | cabelo em chamas, barra de fogo, brasas e orbe solar | Passo de fogo: rastro de chamas | Brasa viva: +12% dano, abates deixam fogo no chão |

No online, os outros jogadores veem o Impulso de cada um.

## Novidades da versão 1.2

- **12 heróis, cada um com um super único** e uma animação de super em tela (faixa com o nome do herói, flash e efeitos próprios): Vaga (Supernova), Lia (Chuva de estrelas), Bento (Bastião sagrado), Mara (Bênção da aurora), Pipa (Bombardeio), Tito (Teia dourada), Íris (Matilha espectral), Ravi (Fúria do trovão), Nina (Protocolo Titã), Dom (Juízo sagrado) e os novos **Kael** (Corte dimensional) e **Sol** (Meteoro solar).
- **O super sempre é o do herói escolhido** (no online, o herói escolhido na sala). Os outros jogadores veem a animação do seu super.
- **Cura online corrigida:** Mara (super e passiva) cura aliados online, levanta quem caiu e deixa uma zona de regeneração; o escudo do Bento também protege os aliados online. Raios, bombas e demais habilidades foram revisados.
- **10 noites** (eram 6), cada uma com cenário, chefe e monstros próprios: Dunas Esquecidas, Caverna de Cristal, Vulcão Ardente e Cidadela Estelar, além de 19 monstros e chefes novos.
- **Desbloqueio de noites pelo progresso salvo no aparelho:** a noite seguinte libera ao passar da metade do tempo da noite atual ou ao vencer. Noites trancadas mostram o motivo ao tocar, e as vencidas ganham ✓. Se o navegador não permitir salvar (aba anônima), o jogo avisa.
- Crédito: "Feito por João Daniel Belarmino" no menu, na pausa, nas telas finais e discreto na tela de jogo.

## Versão 1.1

- **Monstros iguais para todos, ao vivo.** Quem começou a partida (o "host") simula os monstros; os outros recebem a posição deles ~10x por segundo e mandam o dano que causam. Se o host sair ou travar (aba em segundo plano), o servidor passa o posto para outro jogador sem interromper a partida.
- **Dificuldade menor no online:** monstros com menos vida, mais lentos, que causam menos dano e nascem em menor ritmo; cada abate dá mais experiência.
- **Heróis de graça no online.** A escolha online não altera o herói da campanha.
- **Reviver:** o aliado levanta quem caiu ao encostar (0,3 s), e quem caiu volta sozinho em 8 s. A partida só acaba se todos caírem ao mesmo tempo. O level-up online não congela mais o mundo.
- **Clarão** (herói Vaga) recarrega em 14 s (era 34 s).
- **Fim do tempo = vitória:** ao zerar o relógio aparece "Sobreviveu!" com animação. No jogo solo ainda dá para continuar para a próxima noite.
- **Limite do mapa:** arena circular com parede de luz; jogadores e monstros não saem dela.

## Rodar localmente

```bash
npm install
npm start
```

Abra `http://localhost:3000`.

## Publicar no Render

1. Suba o conteúdo deste zip (todos os arquivos na raiz, incluindo o `index.html`) para um repositório, ou use "Deploy from a Git repo".
2. O `render.yaml` já define o serviço: build `npm install`, start `npm start`, health check `/health`.
3. Use o endereço público HTTPS (ex.: `https://seu-jogo.onrender.com`) e passe o código da sala para os amigos.

No plano gratuito o Render "dorme" após alguns minutos sem acesso; a primeira conexão pode demorar até um minuto.

## Observações

- Salas e jogadores ficam em memória; reiniciar o servidor encerra as salas.
- Para produção, restrinja o CORS ao domínio do jogo em `server.js`.
