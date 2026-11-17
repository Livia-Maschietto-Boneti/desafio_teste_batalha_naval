Lívia Maschietto Boneti - 24000749-2 Maria Eduarda Bellarmino Duarte 24036202-2

# Batalha Naval 
# 1. Introdução
A atividade implementa e testa em JavaScript a lógica básica de Batalha Naval em um tabuleiro de 10 × 10 casas. A frota tem quatro navios e ocupa 14 casas ao todo. Os testes automatizados verificam as dimensões, a composição da frota, o posicionamento dos navios e o resultado dos disparos.
Nesta versão, o navio de duas casas é o Destroier. O código impede que navios saiam do tabuleiro ou ocupem a mesma casa; não aplica uma distância mínima entre eles.
# 2. Regras de negócio
# RN01 — Tabuleiro. O tabuleiro tem 10 linhas e 10 colunas.
# RN02 — Frota. Há exatamente um Porta-aviões de 5 casas, um Encouraçado de 4, um Submarino de 3 e um Destroier de 2.
# RN03 — Posicionamento. Cada navio ocupa casas contíguas, na horizontal ou na vertical.
# RN04 — Limites e sobreposição. Navios não podem ultrapassar as bordas nem ocupar casas já usadas.
# RN05 — Início da partida. A partida começa quando todos os navios da frota forem posicionados.
# RN06 — Disparos. Disparos só são aceitos após o posicionamento completo e dentro do tabuleiro. Um mesmo alvo não pode ser contabilizado duas vezes.
# RN07 — Resultado do disparo. Um tiro em casa vazia é água; em casa ocupada é acerto. Um navio afunda quando todos os seus segmentos são atingidos.
# RN08 — Vitória. A partida termina com vitória quando todos os 14 segmentos da frota forem atingidos.
# 3. Casos de teste

# CT01
Criar o tabuleiro
10 linhas, 10 colunas e 100 casas distintas
# CT02
Conferir a frota
Quatro navios com comprimentos 5, 4, 3 e 2
# CT03
Posicionar navio na horizontal
O navio ocupa casas contíguas na linha
# CT04
Posicionar navio na vertical
O navio ocupa casas contíguas na coluna
# CT05
Posicionar navio para fora do tabuleiro
Rejeitar a posição sem ocupar casas parcialmente
# CT06
Sobrepor dois navios
Rejeitar a posição em conflito
# CT07
Informar orientação inválida
Rejeitar orientação diferente de horizontal ou vertical
# CT08
Informar navio inexistente
Rejeitar o identificador
# CT09
Disparar antes de posicionar toda a frota
Rejeitar o disparo
# CT10
Disparar fora do tabuleiro
Rejeitar as coordenadas inválidas
# CT11
Atirar em uma casa sem navio
Registrar água e não aumentar os acertos
# CT12
Atirar em uma casa ocupada
Registrar o acerto e identificar o navio
# CT13
Repetir um disparo
Não contabilizar novamente o tiro nem o acerto
# CT14
Atingir toda a frota
Afundar os navios e encerrar a partida com vitória
