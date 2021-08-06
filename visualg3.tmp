Algoritmo "Jogo_Da_Velha - v1.5"
//        Disciplina : Algoritmos e Lógica de Programação
//         Professor : André Matos
//         Descrição : Jogo da Velha com Inteligência Artificial
//           Autores : Laura Lorrayne Oliveira Reis
//              "    : Luana dos Santos Lima
//              "    : Romilson Júnio Abreu Pereira
//              "    : Vagner Santin
//       Data Início : 07/03/2020
// Data Apresentação : 18/06/2020

Arquivo "frontend.txt"

//FUNÇÃO PARA ENCONTRAR A LETRA A IMPRIMIR/////////////////////////////
funcao posicaoLetra(letra: caracter):inteiro
   inicio
      escolha(maiusc(letra))
         caso "A", "Á", "Ã", "Â"
            retorne 1
         caso "B"
            retorne 2
         caso "C", "Ç"
            retorne 3
         caso "D"
            retorne 4
         caso "E", "É", "Ê"
            retorne 5
         caso "F"
            retorne 6
         caso "G"
            retorne 7
         caso "H"
            retorne 8
         caso "I", "Í"
            retorne 9
         caso "J"
            retorne 10
         caso "K"
            retorne 11
         caso "L"
            retorne 12
         caso "M"
            retorne 13
         caso "N"
            retorne 14
         caso "O", "Ô", "Ó", "Õ"
            retorne 15
         caso "P"
            retorne 16
         caso "Q"
            retorne 17
         caso "R"
            retorne 18
         caso "S"
            retorne 19
         caso "T"
            retorne 20
         caso "U", "Ú", "Ü", "Û"
            retorne 21
         caso "V"
            retorne 22
         caso "W"
            retorne 23
         caso "X"
            retorne 24
         caso "Y"
            retorne 25
         caso "Z"
            retorne 26
         outrocaso
            retorne 27
      fimescolha
   fimfuncao
//FUNÇÃO PARA ENCONTRAR A POSIÇÃO EM QUE O COMPUTADOR PODE JOGAR///////
funcao buscarPosicao(posicaoMelhor: caracter; posicao: inteiro):inteiro
   inicio
      // [ 1 ] - PARA LINHA
      // [ 2 ] - PARA COLUNA
      escolha(posicaoMelhor)
      caso "11"
         se posicao = 1 entao
            retorne 1
         fimse
      caso "12"
         se posicao = 1 entao
            retorne 1
         senao
            retorne 2
         fimse
      caso "13"
         se posicao = 1 entao
            retorne 1
         senao
            retorne 3
         fimse
      caso "21"
         se posicao = 1 entao
            retorne 2
         senao
            retorne 1
         fimse
      caso "22"
         se posicao = 1 entao
            retorne 2
         fimse
      caso "23"
         se posicao = 1 entao
            retorne 2
         senao
            retorne 3
         fimse
      caso "31"
         se posicao = 1 entao
            retorne 3
         senao
            retorne 1
         fimse
      caso "32"
         se posicao = 1 entao
            retorne 3
         senao
            retorne 2
         fimse
      caso "33"
         se posicao = 1 entao
            retorne 3
         fimse
      fimescolha
   fimfuncao
//VERIFICA SE A PEÇA DA RODADA PODE GANHAR O JOGO//////////////////////
//FUNÇÃO PARA OU FORÇAR A VELHA OU FORÇAR O COMPUTADOR A GANHAR SE POSSÍVEL
funcao podeGanhar(peca: caracter):logico
   var
      linha, coluna: inteiro
      podeGanharJogo: logico
   inicio
      podeGanharJogo <- falso
      para linha de 1 ate 3 faca
         se (jogoVelha[linha,1] = peca) e (jogoVelha[linha,2] = peca) e (jogoVelha[linha,3] = textoVazio) entao
            linhaMelhor  <- linha
            colunaMelhor <- 3
            podeGanharJogo <- verdadeiro
         fimse
         se (jogoVelha[linha,1] = peca) e (jogoVelha[linha,2] = textoVazio) e (jogoVelha[linha,3] = peca) entao
            linhaMelhor  <- linha
            colunaMelhor <- 2
            podeGanharJogo <- verdadeiro
         fimse
         se (jogoVelha[linha,1] = textoVazio) e (jogoVelha[linha,2] = peca) e (jogoVelha[linha,3] = peca) entao
            linhaMelhor  <- linha
            colunaMelhor <- 1
            podeGanharJogo <- verdadeiro
         fimse
      fimpara
      para coluna de 1 ate 3 faca
         se (jogoVelha[1,coluna] = peca) e (jogoVelha[2,coluna] = peca) e (jogoVelha[3,coluna] = textoVazio) entao
            linhaMelhor  <- 3
            colunaMelhor <- coluna
            podeGanharJogo <- verdadeiro
         fimse
         se (jogoVelha[1,coluna] = peca) e (jogoVelha[2,coluna] = textoVazio) e (jogoVelha[3, coluna] = peca) entao
            linhaMelhor  <- 2
            colunaMelhor <- coluna
            podeGanharJogo <- verdadeiro
         fimse
         se (jogoVelha[1, coluna] = textoVazio) e (jogoVelha[2, coluna] = peca) e (jogoVelha[3, coluna] = peca) entao
            linhaMelhor  <- 1
            colunaMelhor <- coluna
            podeGanharJogo <- verdadeiro
         fimse
      fimpara
      se (jogoVelha[1,1] = peca) e  (jogoVelha[2,2] = peca) e (jogoVelha[3,3] = textoVazio) entao
         linhaMelhor  <- 3
         colunaMelhor <- 3
         podeGanharJogo <- verdadeiro
      fimse
      se (jogoVelha[1,1] = peca) e  (jogoVelha[2,2] = textoVazio) e (jogoVelha[3,3] = peca) entao
         linhaMelhor  <- 2
         colunaMelhor <- 2
         podeGanharJogo <- verdadeiro
      fimse
      se (jogoVelha[1,1] = textoVazio) e  (jogoVelha[2,2] = peca) e (jogoVelha[3,3] = peca) entao
         linhaMelhor  <- 1
         colunaMelhor <- 1
         podeGanharJogo <- verdadeiro
      fimse
      se (jogoVelha[3,1] = peca) e  (jogoVelha[2,2] = peca) e (jogoVelha[1,3] = textoVazio) entao
         linhaMelhor  <- 1
         colunaMelhor <- 3
         podeGanharJogo <- verdadeiro
      fimse
      se (jogoVelha[3,1] = peca) e  (jogoVelha[2,2] = textoVazio) e (jogoVelha[1,3] = peca) entao
         linhaMelhor  <- 2
         colunaMelhor <- 2
         podeGanharJogo <- verdadeiro
      fimse
      se (jogoVelha[3,1] = textoVazio) e  (jogoVelha[2,2] = peca) e (jogoVelha[1,3] = peca) entao
         linhaMelhor  <- 3
         colunaMelhor <- 1
         podeGanharJogo <- verdadeiro
      fimse
      retorne podeGanharJogo
   fimfuncao
//VERIFICA SE HÁ MELHOR JOGADA PARA O COMPUTADOR REALIZAR//////////////
funcao haMelhorJogada(): logico
   var
      j: inteiro
      melhorJogadaValida, fimJogo: logico
   inicio
      fimJogo <- falso
      melhorJogadaValida <- falso
      se buscarQuantidadeMelhoresJogadas() <> 0 entao
         enquanto (melhorJogadaValida = falso) e (fimJogo = falso) faca
            se (rodada = 1) ou (rodada = 2) entao
               linhaEstatica <- buscarQuantidadeMelhoresJogadas()
               linhaEstatica <- Randi(linhaEstatica)+1
               linhaInicial  <- linhaEstatica
            fimse
            linhaMelhor  <- buscarPosicao(melhorJogada[linhaEstatica, comp], 1)//1 é linha
            colunaMelhor <- buscarPosicao(melhorJogada[linhaEstatica, comp], 2)//2 é coluna
            se (linhaMelhor = 1) ou (linhaMelhor = 2) ou (linhaMelhor = 3) e (colunaMelhor = 1) ou (colunaMelhor = 2) ou (colunaMelhor = 3) entao
               melhorJogadaValida <- verificarJogada(linhaMelhor, colunaMelhor)
               se  melhorJogadaValida = verdadeiro entao
                  jogadas[linhaJogadas] <- numPCarac(linhaMelhor) + numPCarac(colunaMelhor)
                  linhaJogadas <- linhaJogadas + 1
               senao
                  melhorJogadaValida <- falso
                  j <- verificarJogadasAnteriores()
                  se j = 150 entao
                     interrompa
                  fimse
               fimse
            senao
               fimJogo <- verdadeiro
            fimse
         fimenquanto
      fimse
      retorne melhorJogadaValida
   fimfuncao
//VERIFICA QUANTAS MELHORES JOGADAS O COMPUTADOR PODE REALIZAR////////
funcao buscarQuantidadeMelhoresJogadas():inteiro
   var
      i: inteiro
   inicio
      para i de 0 ate 149 faca
         se (melhorJogada[i+1,1] = " ") entao
            //Retorna a quantidade de melhores jogadas cadastradas
            retorne i
            interrompa
         fimse
      fimpara
   fimfuncao
//VERIFICA AS JOGADAS ANTERIORES DO COMPUTADOR/////////////////////////
funcao verificarJogadasAnteriores(): inteiro
   var
      j, i: inteiro
   inicio
      se linhaEstatica = linhaInicial entao
         i <- 1
      senao
         i <- linhaEstatica + 1
      fimse
      para j de i ate melhoresJogadas faca
         se j <> linhaInicial entao
            escolha(comp)
            caso 2
               se (melhorJogada[j,1] = jogadas[1]) entao
                  linhaEstatica <- j
                  interrompa
               fimse
            caso 3
               se (melhorJogada[j,1] = jogadas[1]) e (melhorJogada[j,2] = jogadas[2]) entao
                  linhaEstatica <- j
                  interrompa
               fimse
            caso 4
               se (melhorJogada[j,1] = jogadas[1]) e (melhorJogada[j,2] = jogadas[2]) e (melhorJogada[j,3] = jogadas[3]) entao
                  linhaEstatica <- j
                  interrompa
               fimse
            caso 5
               se (melhorJogada[j,1] = jogadas[1]) e (melhorJogada[j,2] = jogadas[2]) e (melhorJogada[j,3] = jogadas[3]) e (melhorJogada[j,4] = jogadas[4]) entao
                  linhaEstatica <- j
                  interrompa
               fimse
            fimescolha
         fimse
      fimpara
      retorne j
   fimfuncao
//VERIFICA SE HÁ VENCEDOR NO JOGO//////////////////////////////////////
funcao haVencedor():logico
   var
      i: inteiro
      temVencedor: logico
   inicio
      temVencedor <- falso
      para i de 1 ate 3 faca
         se (jogoVelha[i,1] = textoO) e (jogoVelha[i,2] = textoO) e (jogoVelha[i, 3] = textoO) entao
            temVencedor <- verdadeiro
         fimse
         se (jogoVelha[i,1] = textoX) e (jogoVelha[i,2] = textoX) e (jogoVelha[i, 3] = textoX) entao
            temVencedor <- verdadeiro
         fimse
         se (jogoVelha[1,i] = textoO) e (jogoVelha[2,i] = textoO) e (jogoVelha[3, i] = textoO) entao
            temVencedor <- verdadeiro
         fimse
         se (jogoVelha[1,i] = textoX) e (jogoVelha[2,i] = textoX) e (jogoVelha[3, i] = textoX) entao
            temVencedor <- verdadeiro
         fimse
      fimpara

      se (jogoVelha[1,1] = textoO) e (jogoVelha[2,2] = textoO) e (jogoVelha[3, 3] = textoO) entao
         temVencedor <- verdadeiro
      fimse
      se (jogoVelha[1,1] = textoX) e (jogoVelha[2,2] = textoX) e (jogoVelha[3, 3] = textoX) entao
         temVencedor <- verdadeiro
      fimse
      se (jogoVelha[3,1] = textoO) e (jogoVelha[2,2] = textoO) e (jogoVelha[1, 3] = textoO) entao
         temVencedor <- verdadeiro
      fimse
      se (jogoVelha[3,1] = textoX) e (jogoVelha[2,2] = textoX) e (jogoVelha[1, 3] = textoX) entao
         temVencedor <- verdadeiro
      fimse
      se temVencedor = verdadeiro entao
         se tipoJogo = COMPUTADOR entao
            se jogoComputador = ADVERSARIO entao
               vencedor <- COMPUTADOR
            senao
               vencedor <- ADVERSARIO
            fimse
         fimse
      fimse
      retorne temVencedor
   fimfuncao
//VERIFICA SE A JOGADA DESEJADA É VÁLIDA///////////////////////////////
funcao verificarJogada(linha, coluna: inteiro):logico
   inicio
      se (jogoVelha[linha, coluna] = textoVazio) entao
         //Se a posição onde deseja jogar estiver vazia
         //retorna que a jogada é válida
         retorne verdadeiro
      senao
         retorne falso
      fimse
   fimfuncao
//VERIFICA SE O NOME DO JOGADOR INFORMADO É VÁLIDO////////////////////
funcao nomeEValido(nome: caracter):logico
   var
      numero,i,j,linha, coluna: inteiro
      letra: caracter
      status: logico
   inicio
      status <- verdadeiro
      numero <- compr(nome)
      se nome = "" entao
         status <- falso
         escreval("ATENÇÃO - NOME NÃO PODE SER VAZIO")
      senao
         se (tipoJogo = ADVERSARIO) e (player1[1] = player2[1]) entao
            status <- falso
            se equipeOuIndividual = "EQUIPE" entao
               escreval("ATENÇÃO - NOME NÃO PODE SER O MESMO DA 1ª EQUIPE")
            senao
               escreval("ATENÇÃO - NOME NÃO PODE SER O MESMO DO 1º JOGADOR")
            fimse
         senao
            para i de 1 ate numero faca
               letra <- copia(nome,i,1)
               //Verifica se tem número no nome
               se (letra = "1") ou (letra = "2") ou (letra = "3") ou (letra = "4") ou (letra = "5") ou (letra = "6") ou (letra = "7") ou (letra = "8") ou (letra = "9") ou (letra = "0") entao
                  status <- falso
                  escreval("ATENÇÃO - NOME NÃO PODE CONTER NÚMEROS")
               fimse
            fimpara
         fimse
      fimse
      retorne status
   fimfuncao
//VERIFICA QUANTAS MELHORES JOGADAS O COMPUTADOR PODE REALIZAR////////
funcao buscarQuantidadeJogadores():inteiro
   var
      i: inteiro
   inicio
      para i de 0 ate 149 faca
         se (Jogadores[i+1,1] = "") entao
            //Retorna a quantidade de jogadores cadastrados
            retorne i
            interrompa
         fimse
      fimpara
   fimfuncao
// Função para adicionar nome do jogador ao jogo
// E retorna a posição em que está armazenado
funcao adicionarJogador(nome: caracter):inteiro
   var
   i, cadastrados, id, qtdJogos: inteiro
   nomeCadastrado: logico
   numJogos: caracter
   inicio
      nomeCadastrado <- falso
      cadastrados <- buscarQuantidadeJogadores()
      se cadastrados <> 0 entao
         para i de 1 ate cadastrados faca
            se maiusc(Jogadores[i,1]) = maiusc(nome) entao
               nomeCadastrado <- verdadeiro
               numJogos <- Jogadores[i,3]
               qtdJogos <- CaracPNum(numJogos) + 1
               Jogadores[i,3] <- NumPCarac(qtdJogos)
               id <- i
               interrompa
            fimse
         fimpara
      fimse
      se nao nomeCadastrado entao
         Jogadores[indiceJogadores,1] <- nome  //Nome Jogador
         Jogadores[indiceJogadores,2] <- "0"   //Pontos
         Jogadores[indiceJogadores,3] <- "1"   //Partidas
         Jogadores[indiceJogadores,4] <- "0"   //Movimentos
         id <- indiceJogadores
         indiceJogadores <- indiceJogadores + 1
      fimse
      retorne id
   fimfuncao
//PROCEDIMENTO PARA ZERAR JOGO ////////////////////////////////////////
procedimento zerarJogo()
   var
      i, j: inteiro
   inicio
      para i de 1 ate 3 faca
         para j de 1 ate 3 faca
            jogoVelha[i, j] <- textoVazio
         fimpara
      fimpara
      linhaJogadas <- 1
      rodada <- 1
      comp <- 0
      auxO <- 1
      auxX <- 1
      se tipoJogo = COMPUTADOR entao
         se iniciaComputador entao
            iniciaComputador <- falso
         senao
            iniciaComputador <- verdadeiro
         fimse
      fimse
      player1[1] <- "VAZIO"
      player2[1] <- "VAZIO"
      player1[3] <- "0"
      player2[3] <- "0"
      cadastrado <- falso
      para i de 1 ate 5 faca
         vetorO[i] <- " "
         vetorX[i] <- " "
      fimpara
   fimprocedimento
//PROCEDIMENTO MOSTRAR TELA ///////////////////////////////////////////
procedimento telaJogo(linha: inteiro)
   var
      posicao, nome: caracter
      coluna: inteiro
   inicio
      nome <- " "
      escolha(linha)
         caso 1
            posicao <- "A"
         caso 2
            posicao <- "B"
         caso 3
            posicao <- "C"
      fimescolha
      se linha = 1 entao
         escreval("                1                            2                            3")
      fimse
      para i de 1 ate 9 faca
         para coluna de 1 ate 3 faca
            se (coluna = 1) e (i = 1) entao
               escreva("            ",posicao,"  ")
            senao
               se coluna = 1 entao
                  escreva("               ")
               fimse
            fimse
            se jogoVelha[linha, coluna] = textoVazio entao
               escreva(pecaVazia)
            fimse
            se jogoVelha[linha, coluna] = textoX entao
               escreva(pecaX[i])
            fimse
            se jogoVelha[linha, coluna] = textoO entao
               escreva(pecaO[i])
            fimse
            se coluna = 3 entao
               se linha = 1 entao
                  se jogador = textoO entao
                     escreval("               ", pecaO[i])
                  senao
                     escreval("               ", pecaX[i])
                  fimse
               senao
                  escreval("")
               fimse
            senao
               escreva("|")
            fimse
         fimpara
      fimpara
      se linha <> 3 entao
         se player1[2] = jogador entao
            nome <- player1[1]
         senao
            se tipoJogo <> COMPUTADOR entao
               nome <- player2[1]
            fimse
         fimse
         se linha = 1 entao
            escreval("               ","______________________________________________________________________________________                         ",maiusc(nome))
         senao
            escreval("               ","______________________________________________________________________________________")
         fimse
      fimse
   fimprocedimento
///////////////////////////////////////////////////////////////////////
procedimento recebeJogadas()
   var
      linha, ultimaJogada, aux, aux1: caracter
      linhaJogada, colunaJogada, qtd: inteiro
      resposta, jogadaValida, computadorPodeGanhar, adversarioPodeGanhar: logico
   inicio
      se (tipoJogo = COMPUTADOR) e (jogoComputador = COMPUTADOR) entao
         comp <- comp + 1
      fimse
      //Repete todo bloco, até que a jogada seja válida
      Repita
         se (tipoJogo = COMPUTADOR) e (jogoComputador = COMPUTADOR) entao
            computadorPodeGanhar <- podeGanhar(pecaComputador)
            se (computadorPodeGanhar = verdadeiro) entao
               linhaJogada  <- linhaMelhor
               colunaJogada <- colunaMelhor
            senao
               adversarioPodeGanhar <- podeGanhar(pecaAdversario)
               se (adversarioPodeGanhar = verdadeiro) entao
                  linhaJogada  <- linhaMelhor
                  colunaJogada <- colunaMelhor
               senao
                  se haMelhorJogada = verdadeiro entao
                     linhaJogada  <- linhaMelhor
                     colunaJogada <- colunaMelhor
                  senao
                     linhaJogada  <- Randi(3) + 1
                     colunaJogada <- Randi(3) + 1
                  fimse
               fimse
            fimse
         senao
            //Repita Linha
            Repita
               resposta <- verdadeiro
               Escreval("Informe a linha [A | B | C]")
               leia(linha)
               escolha(maiusc(linha))
                  caso "A"
                     linhaJogada <- 1
                  caso "B"
                     linhaJogada <- 2
                  caso "C"
                     linhaJogada <- 3
                  outrocaso
                     escreval("OPCAO INFORMADA NÃO CORRESPONDENTE! DIGITE UMA OPÇÃO VALIDA!")
                     resposta <- falso
               fimescolha
            ate(resposta = verdadeiro)

            //Repita Coluna
            Repita
               resposta <- verdadeiro
               Escreval("Informe a coluna [1 | 2 | 3]")
               leia(colunaJogada)
               se (colunaJogada <> 1) e (colunaJogada <> 2) e (colunaJogada <> 3) entao
                  escreval("OPCAO INFORMADA NÃO CORRESPONDENTE! DIGITE UMA OPÇÃO VALIDA!")
                  resposta <- falso
               fimse
            ate(resposta = verdadeiro)
         fimse
         jogadaValida <- verificarJogada(linhaJogada, colunaJogada)
         se jogadaValida = verdadeiro entao
            se jogador = textoO entao
               se player1[2] = textoO entao
                   aux <- player1[3]
                   qtd <- CaracPNum(aux) + 1
                   player1[3] <- NumPCarac(qtd)
               senao
                   aux <- player2[3]
                   qtd <- CaracPNum(aux) + 1
                   player2[3] <- NumPCarac(qtd)
               fimse
               ultimaJogada <- textoO
               vetorO[auxO] <- numPCarac(linhaJogada) + numPCarac(colunaJogada)
               auxO <- auxO + 1
               jogoVelha[linhaJogada, colunaJogada] <- jogador
               jogador <- textoX
               mudacor("azul", "fundos")
            senao
               se player1[2] = textoX entao
                   aux <- player1[3]
                   qtd <- CaracPNum(aux) + 1
                   player1[3] <- NumPCarac(qtd)
               senao
                   aux <- player2[3]
                   qtd <- CaracPNum(aux) + 1
                   player2[3] <- NumPCarac(qtd)
               fimse
               ultimaJogada <- textoX
               vetorX[auxX] <- numPCarac(linhaJogada) + numPCarac(colunaJogada)
               auxX <- auxX + 1
               jogoVelha[linhaJogada, colunaJogada] <- jogador
               jogador <- textoO
               mudacor("verde", "fundos")
               se (tipoJogo = COMPUTADOR) e (jogoComputador = ADVERSARIO) entao
                   aux <- player1[3]
                   qtd <- CaracPNum(aux) + 1
                   player1[3] <- NumPCarac(qtd)
               fimse
            fimse
            //Troca a vez do jogador e do computador
            se tipoJogo = COMPUTADOR entao
               se jogoComputador = COMPUTADOR entao
                  jogoComputador <- ADVERSARIO
               senao
                  jogoComputador <- COMPUTADOR
               fimse
            fimse
            rodada <- rodada + 1
         senao
            se jogoComputador <> COMPUTADOR  entao
               escreval("JOGADA INVÁLIDA, TENTE NOVAMENTE!")
            fimse
         fimse
   ate(jogadaValida = verdadeiro)
   se haVencedor() = verdadeiro entao
      tela()
      pularLinha(1)
      cadastrado <- falso
      se tipoJogo = COMPUTADOR entao
         se vencedor = COMPUTADOR entao
            apresentarMensagem(" COMPUTADOR VENCEU ")
         senao
            apresentarMensagem(" "+player1[1]+" VENCEU ")
            winer(player1[1])
            //incluir a pontuação, se vencer o computador ganha 2 pontos
            incluirPontuacao(idJogador1,pontosComp)//Passa o ID do vencedor e apontuação
            aux <- Jogadores[idJogador1,4]
            aux1 <- player1[3]
            qtd <- CaracPNum(aux) + CaracPNum(aux1)
            Jogadores[idJogador1,4] <- NumPCarac(qtd)
         fimse
      senao
         se player1[2] = ultimaJogada entao
            apresentarMensagem(" "+player1[1]+" VENCEU ")
            winer(player1[1])
            //incluir a pontuação, se vencer o adversário ganha 1 ponto
            incluirPontuacao(idJogador1,pontosAdv)//Passa o ID do vencedor e apontuação
            aux <- Jogadores[idJogador1,4]
            aux1 <- player1[3]
            qtd <- CaracPNum(aux) + CaracPNum(aux1)
            Jogadores[idJogador1,4] <- NumPCarac(qtd)
         senao
            apresentarMensagem(" "+player2[1]+" VENCEU ")
            winer(player2[1])
            //incluir a pontuação, se vencer o adversário ganha 1 ponto
            incluirPontuacao(idJogador2,pontosAdv)//Passa o ID do vencedor e apontuação
            aux <- Jogadores[idJogador2,4]
            aux1 <- player2[3]
            qtd <- CaracPNum(aux) + CaracPNum(aux1)
            Jogadores[idJogador2,4] <- NumPCarac(qtd)
         fimse
      fimse
      ultimaMelhorJogada <- buscarQuantidadeMelhoresJogadas()
      se ultimaJogada = textoX entao
         se ultimaMelhorJogada = 0 entao
            para i de 1 ate 5 faca
               melhorJogada[ultimaMelhorJogada+1,i] <- vetorX[i]
            fimpara
         senao
            para j de 1 ate ultimaMelhorJogada faca
               cont <- 0
               se nao cadastrado entao
                  para p de 1 ate 5 faca
                     se melhorJogada[j,p] = vetorX[p] entao
                        cont <- cont + 1
                     fimse
                  fimpara
                  se cont = 5 entao
                     cadastrado <- verdadeiro
                  fimse
               fimse
            fimpara
            se nao cadastrado entao
               para i de 1 ate 5 faca
                  melhorJogada[ultimaMelhorJogada+1,i] <- vetorX[i]
               fimpara
            fimse
         fimse
      fimse
      se ultimaJogada = textoO entao
         se ultimaMelhorJogada = 0 entao
            para i de 1 ate 5 faca
               melhorJogada[ultimaMelhorJogada+1,i] <- vetorO[i]
            fimpara
         senao
            para j de 1 ate ultimaMelhorJogada faca
               cont <- 0
               se nao cadastrado entao
                  para p de 1 ate 5 faca
                     se melhorJogada[j,p] = vetorO[p] entao
                        cont <- cont + 1
                     fimse
                  fimpara
                  se cont = 5 entao
                     cadastrado <- verdadeiro
                  fimse
               fimse
            fimpara
            se nao cadastrado entao
               para i de 1 ate 5 faca
                  melhorJogada[ultimaMelhorJogada+1,i] <- vetorO[i]
               fimpara
            fimse
         fimse
      fimse
      pularLinha(1)
      escreval("VER RANKING [ APERTE ENTER ]")
      leia(continuar)
      montarRanking()
   fimse
   fimprocedimento
///////////////////////////////////////////////////////////////////////
procedimento continuar()
   inicio
      escreval("JOGAR NOVAMENTE, APERTE [ENTER]")
      escreval("SAIR, APERTE [ESC]")
      leia(continuar)
      limpatela()
      mudacor("verde","fundos")
      zerarJogo()
      escolheJogo()
   fimprocedimento
///////////////////////////////////////////////////////////////////////
procedimento pularLinha(linhas: inteiro)
   var
      j: inteiro
   inicio
      para j de 1 ate linhas faca
         escreval("")
      fimpara
   fimprocedimento
///////////////////////////////////////////////////////////////////////
procedimento tela()
   inicio
      limpatela()
      telaJogo(1)
      telaJogo(2)
      telaJogo(3)
   fimprocedimento
// Procedimento para incluir pontuação ao vencedor
procedimento incluirPontuacao(id, pontuacao:inteiro)
   var
      quantidade: inteiro
      pontos: caracter
   inicio
      pontos <- Jogadores[id,2]
      quantidade <- CaracPNum(pontos) + pontuacao
      Jogadores[id,2] <- NumPCarac(quantidade)
   fimprocedimento
//Procedimento escolher jogo contra compputador ou adversaio
procedimento escolheJogo()
   var
      opcao: inteiro
      valido: logico
   inicio
      empate()
      para i de 1 ate 12 faca
         escreval(tela[i])
      fimpara
      apresentarMensagem("                               JOGAR                                ")
      //apresentarMensagem("   CONTRA  COMPUTADOR  I        ")
      //apresentarMensagem("   CONTRA  ADVERSARIO  II    ")
      escreval("INFORME A OPÇÃO")
      escreval("[1] PARA CONTRA COMPUTADOR   -   VITÓRIA GANHA ",pontosComp," PONTOS")
      escreval("[2] PARA CONTRA ",equipeOuIndividual,"  -   VITÓRIA GANHA ",pontosAdv ," PONTO ")
      se(buscarQuantidadeJogadores() > 0)entao
          escreval("[3] RANKING")
      fimse
      tipoJogo <- ""
      repita
         leia(opcao)
         escolha(opcao)
         caso 1
            valido <- falso
            tipoJogo <- COMPUTADOR
            //jogoComputador <- COMPUTADOR
            repita
               se equipeOuIndividual = "EQUIPE" entao
                  escreval("INFORME NOME DA EQUIPE")
               senao
                  escreval("INFORME NOME DO JOGADOR")
               fimse

               leia(player1[1])
               valido <- nomeEValido(player1[1])
               se nao valido  entao
                  escreval("NOME INVÁLIDO")
               fimse
            ate valido
            idJogador1 <- adicionarJogador(maiusc(player1[1]))
         caso 2
            valido <- falso
            tipoJogo <- ADVERSARIO
            jogoComputador <- ADVERSARIO
            repita
               se equipeOuIndividual = "EQUIPE" entao
                  escreval("INFORME O NOME DA 1ª EQUIPE")
               senao
                  escreval("INFORME O NOME DO 1º JOGADOR")
               fimse
               leia(player1[1])
               valido <- nomeEValido(player1[1])
               se nao valido entao
                  escreval("NOME INVÁLIDO")
               fimse
            ate valido
            valido <- falso
            repita
               se equipeOuIndividual = "EQUIPE" entao
                  escreval("INFORME O NOME DA 2ª EQUIPE")
               senao
                  escreval("INFORME O NOME DO 2º JOGADOR")
               fimse
               leia(player2[1])
               valido <- nomeEValido(player2[1])
               se nao valido entao
                  escreval("NOME INVÁLIDO")
               fimse
            ate valido
            idJogador1 <- adicionarJogador(maiusc(player1[1]))
            idJogador2 <- adicionarJogador(maiusc(player2[1]))
         caso 3
              se(buscarQuantidadeJogadores() > 0)entao
                 montarRanking()
              senao
                 escreval("OPÇÃO INVÁLIDA! DIGITE NOVAMENTE")
                 tipoJogo <- "INVALIDA"
              fimse
         outrocaso
            escreval("OPÇÃO INVÁLIDA! DIGITE NOVAMENTE")
            tipoJogo <- "INVALIDA"
         fimescolha
      ate(tipoJogo <> "INVALIDA")
      iniciarJogadores()
      rotina <- rotina + 1
   fimprocedimento
///////////////////////////////////////////////////////////////////////
procedimento apresentarMensagem(msg: caracter)
   var
      numero,i,j,linha, coluna: inteiro
      letra: caracter
   inicio
      numero <- compr(msg)
      coluna <- 1
      repita
         para i de 1 ate numero faca
            letra <- copia(msg,i,1)
            linha <- posicaoLetra(letra)
            escreva(alfabeto[linha,coluna])
         fimpara
         coluna <- coluna + 1
         pularLinha(1)
      ate(coluna = 10)
   fimprocedimento
procedimento winer(vencedor: caracter)
var
   i: inteiro
   
   inicio
      pularLinha(1)
      escreval("__________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶__________________________________________")
      escreval("__________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶__________________________________________")
      escreval("_____________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶____________________________________")
      escreval("___________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶__________________________________")
      escreval("__________________________________¶¶¶¶______¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶_______¶¶¶¶_________________________________")
      escreval("__________________________________¶¶¶_______¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶________¶¶¶_________________________________")
      escreval("__________________________________¶¶________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶________¶¶¶_________________________________")
      escreval("__________________________________¶¶¶_____¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶______¶¶¶_________________________________")
      escreval("__________________________________¶¶¶____¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶____¶¶¶¶_________________________________")
      escreval("___________________________________¶¶¶___¶¶¶_¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶_¶¶¶____¶¶¶__________________________________")
      escreval("___________________________________¶¶¶¶___¶¶¶_¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶_¶¶¶¶__¶¶¶¶___________________________________")
      escreval("_____________________________________¶¶¶¶__¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶_¶¶¶¶¶____________________________________")
      escreval("______________________________________¶¶¶¶¶¶¶¶_¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶_¶¶¶¶¶¶¶¶¶_____________________________________")
      escreval("________________________________________¶¶¶¶¶¶__¶¶¶¶¶¶¶¶¶¶¶¶¶¶___¶¶¶¶¶¶_______________________________________")
      escreval("_________________________________________________¶¶¶¶¶¶¶¶¶¶¶¶_________________________________________________")
      escreval("___________________________________________________¶¶¶¶¶¶¶¶___________________________________________________")
      escreval("_____________________________________________________¶¶¶¶_____________________________________________________")
      escreval("_____________________________________________________¶¶¶¶_____________________________________________________")
      escreval("_____________________________________________________¶¶¶¶_____________________________________________________")
      escreval("_____________________________________________________¶¶¶¶_____________________________________________________")
      escreval("_________________________________________________¶¶¶¶¶¶¶¶¶¶¶¶_________________________________________________")
      escreval("______________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶______________________________________________")
      escreval("______________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶______________________________________________")
      escreval("______________________________________________¶¶¶____________¶¶¶______________________________________________")
      escreval("______________________________________________¶¶¶____________¶¶¶______________________________________________")
      escreval("______________________________________________¶¶¶____________¶¶¶______________________________________________")
      escreval("______________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶______________________________________________")
      escreval("______________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶______________________________________________")
      escreval("____________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶____________________________________________")
      escreval("___________________________________________¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶¶___________________________________________")

   fimprocedimento
   
// Procedimento para montar o ranking
procedimento montarRanking()
   var
   i, l, c, cadastrados, pontosPrimeiro, pontosSegundo, aux: inteiro
   jogadasPri, jogadasSeg, jogAux, tentativaPri, tentativaSeg, tenAux: inteiro
   pri, sec, ter: caracter
   ranking: vetor[1..150,1..4] de caracter
   nome1, nome2, nomeAux: caracter
   inicio
   mudacor("preto","fundos")
   para i de 1 ate 150 faca
     ranking[i,1] <- Jogadores[i,1]
     ranking[i,2] <- Jogadores[i,2]
     ranking[i,3] <- Jogadores[i,3]
     ranking[i,4] <- Jogadores[i,4]
   fimpara
   cadastrados <- buscarQuantidadeJogadores()
   se cadastrados <> 0 entao
      para i de 1 ate cadastrados faca
        para j de i+1 ate cadastrados faca
          pontosPrimeiro <- CaracPNum(ranking[i,2])
          nome1 <- ranking[i,1]
          jogadasPri <- CaracPNum(ranking[i,3])
          tentativaPri <- CaracPNum(ranking[i,4])
          
          pontosSegundo  <- CaracPNum(ranking[j,2])
          nome2 <- ranking[j,1]
          jogadasSeg <- CaracPNum(ranking[j,3])
          tentativaSeg <- CaracPNum(ranking[j,4])
          
          se pontosPrimeiro < pontosSegundo entao
            aux <- pontosPrimeiro
            nomeAux <- nome1
            jogAux <- jogadasPri
            tenAux <- tentativaPri

            pontosPrimeiro <- pontosSegundo
            nome1 <- nome2
            jogadasPri <- jogadasSeg
            tentativaPri <- tentativaSeg
            
            pontosSegundo <- aux
            nome2 <- nomeAux
            jogadasSeg <- jogAux
            tentativaSeg <- tenAux

            ranking[i,1] <- nome1
            ranking[i,2] <- NumPcarac(pontosPrimeiro)
            ranking[i,3] <- NumPcarac(jogadasPri)
            ranking[i,4] <- NumPcarac(tentativaPri)

            ranking[j,1] <- nome2
            ranking[j,2] <- NumPcarac(pontosSegundo)
            ranking[j,3] <- NumPcarac(jogadasSeg)
            ranking[j,4] <- NumPcarac(tentativaSeg)
          senao
            se pontosPrimeiro = pontosSegundo entao
               se jogadasPri > jogadasSeg entao
                  aux <- pontosPrimeiro
                  nomeAux <- nome1
                  jogAux <- jogadasPri
                  tenAux <- tentativaPri

                  pontosPrimeiro <- pontosSegundo
                  nome1 <- nome2
                  jogadasPri <- jogadasSeg
                  tentativaPri <- tentativaSeg

                  pontosSegundo <- aux
                  nome2 <- nomeAux
                  jogadasSeg <- jogAux
                  tentativaSeg <- tenAux
               
                  ranking[i,1] <- nome1
                  ranking[i,2] <- NumPcarac(pontosPrimeiro)
                  ranking[i,3] <- NumPcarac(jogadasPri)
                  ranking[i,4] <- NumPcarac(tentativaPri)

                  ranking[j,1] <- nome2
                  ranking[j,2] <- NumPcarac(pontosSegundo)
                  ranking[j,3] <- NumPcarac(jogadasSeg)
                  ranking[j,4] <- NumPcarac(tentativaSeg)
               senao
                 se jogadasPri = jogadasSeg entao
                    se tentativaPri > tentativaSeg entao
                        aux <- pontosPrimeiro
                        nomeAux <- nome1
                        jogAux <- jogadasPri
                        tenAux <- tentativaPri

                        pontosPrimeiro <- pontosSegundo
                        nome1 <- nome2
                        jogadasPri <- jogadasSeg
                        tentativaPri <- tentativaSeg

                        pontosSegundo <- aux
                        nome2 <- nomeAux
                        jogadasSeg <- jogAux
                        tentativaSeg <- tenAux

                        ranking[i,1] <- nome1
                        ranking[i,2] <- NumPcarac(pontosPrimeiro)
                        ranking[i,3] <- NumPcarac(jogadasPri)
                        ranking[i,4] <- NumPcarac(tentativaPri)

                        ranking[j,1] <- nome2
                        ranking[j,2] <- NumPcarac(pontosSegundo)
                        ranking[j,3] <- NumPcarac(jogadasSeg)
                        ranking[j,4] <- NumPcarac(tentativaSeg)
                    fimse
                 fimse
               fimse
            fimse
          fimse
        fimpara
      fimpara

      limpatela()
      apresentarMensagem("          RANKING          ")
      escreval("################################################################################################")
      escreva("#   POSIÇÃO            ")
      se equipeOuIndividual = "EQUIPE" entao
         escreva(equipeOuIndividual," ")
      senao
         escreva("JOGADOR")
      fimse

      escreval("             PONTOS             PARTIDAS                         #")
      escreval("#______________________________________________________________________________________________#")
      escreval("#                                                                                              #")
      para i de 1 ate cadastrados faca
         se i > 10 entao
              interrompa
         fimse
         escreva("#   ",i:2,"º                ",ranking[i,1])
         complementoNome(ranking[i,1])
         escreval(CaracPNum(ranking[i,2]):2," .................",CaracPNum(ranking[i,3]):2,"                             #")
      fimpara
      escreval("#                                                                                              #")
      escreval("################################################################################################")
      pularLinha(1)
      se(CaracPNum(ranking[1,2]) > 0) entao
         apresentarMensagem("        "+ranking[1,1]+"        ")
      fimse
      pularLinha(1)
      continuar()
   fimse
   fimprocedimento
procedimento complementoTaca(nome: caracter)
   var
   i, espacos: inteiro
   inicio
   espacos <- compr(nome)
      para i de espacos ate 12 faca
           escreva("_")
      fimpara
   fimprocedimento


procedimento complementoNome(nome: caracter)
   var
   i, espacos: inteiro
   inicio
   espacos <- compr(nome)
   para i de espacos ate 20 faca
        escreva(".")
   fimpara
   fimprocedimento
// INICIA AS PEÇAS DOS JOGADORES //////////////////////////////////////
procedimento iniciarJogadores()
   var
   inicio
            
      se (rodada = 1) e (tipoJogo = COMPUTADOR) entao
         se (iniciaComputador) entao
             jogoComputador <- COMPUTADOR
             jogador <- textoO
             pecaComputador <- jogador
             pecaAdversario <- textoX
             player1[2] <- pecaAdversario
         senao
             jogoComputador <- ADVERSARIO
             jogador <- textoO
             pecaComputador <- textoX
             pecaAdversario <- jogador
             player1[2] <- pecaAdversario
         fimse
         player1[3] <- "0"
      fimse
      se (rodada = 1) e (tipoJogo = ADVERSARIO) entao
        se (rotina mod 2 = 0) entao
           player1[2] <- textoO
           player2[2] <- textoX
           jogador <- textoO
        senao
           player2[2] <- textoO
           player1[2] <- textoX
           jogador <- textoX
        fimse
      fimse
   fimprocedimento
//DEFINE PONTUAÇÃO PARA EMPATE ////////////////////////////////
procedimento empate()
   var
   inicio
      se permitirEmpate entao
         pontosComp <- 3
         pontosAdv  <- 2
      senao
         pontosComp <- 2
         pontosAdv  <- 1
      fimse
   fimprocedimento
procedimento painelInicial()
   var
   op, i: inteiro
   inicio
         //escreval("########################################")
         //escreval("########################################")
         //escreval("#####      ##      ##      ##      #####")
        // escreval("#######  ######  ####  ##  ##  ##  #####")
        // escreval("#######  ######  ####      ##  ##  #####")
        // escreval("#######  ######  ####  ######  ##  #####")
         //escreval("#######  ####      ##  ######      #####")
         //escreval("########################################")
         //escreval("########################################")
         para i de 1 ate 12 faca
         escreval(tela[i])
         fimpara
          escreval(tela[1])
          escreval(tela[2])
         pularLinha(1)
         escreval("SELECIONE O TIPO DE JOGO")
         escreval("[1] EQUIPE")
         escreval("[2] INDIVIDUAL")
         repita
               leia(op)
         ate (op = 1) ou (op = 2)
         escolha(op)
            caso 1
                  equipeOuIndividual <- "EQUIPE"

            caso 2
                 equipeOuIndividual <- "ADVERSARIO"
         fimescolha
         limpatela()
   fimprocedimento
procedimento nivelJogo()
   var
   op, i: inteiro
   inicio
         //escreval("################################################")
         //escreval("################################################")
         //escreval("#####  ##  ##      ##  ##  ##      ##  #########")
         //escreval("#####   #  ####  ####  ##  ##  ######  #########")
         //escreval("#####      ####  ####  ##  ##     ###  #########")
         //escreval("#####  #   ####  #####    ###  ######  #########")
         //escreval("#####  ##  ##      ####  ####      ##      #####")
         //escreval("################################################")
         //escreval("################################################")
         para i de 1 ate 12 faca
         escreval(tela[i])
         fimpara
          escreval(tela[1])
          escreval(tela[2])
         pularLinha(1)
         
         escreval("SELECIONE UM NÍVEL")
         escreval("[1] FÁCIL")
         escreval("[2] MÉDIO")
         escreval("[3] DIFÍCIL")
         repita
               leia(op)
         ate (op = 1) ou (op = 2) ou (op = 3)
         escolha(op)
            caso 1
                 //Segue o fluxo
            caso 2
                 matrizMelhorJogadaMedia()
            caso 3
                 matrizMelhorJogadaDificil()
         fimescolha
         limpatela()

fimprocedimento
procedimento matrizMelhorJogadaMedia()
   var
   inicio
          melhorJogada[1,1] <- "11"
          melhorJogada[1,2] <- "22"
          melhorJogada[1,3] <- "33"
          melhorJogada[2,1] <- "11"
          melhorJogada[2,2] <- "12"
          melhorJogada[2,3] <- "13"
          melhorJogada[3,1] <- "21"
          melhorJogada[3,2] <- "22"
          melhorJogada[3,3] <- "23"
          melhorJogada[4,1] <- "31"
          melhorJogada[4,2] <- "32"
          melhorJogada[4,3] <- "33"
          melhorJogada[5,1] <- "11"
          melhorJogada[5,2] <- "21"
          melhorJogada[5,3] <- "31"
          melhorJogada[6,1] <- "12"
          melhorJogada[6,2] <- "22"
          melhorJogada[6,3] <- "32"
          melhorJogada[7,1] <- "13"
          melhorJogada[7,2] <- "23"
          melhorJogada[7,3] <- "33"
fimprocedimento
procedimento matrizMelhorJogadaDificil()
   var
   inicio
        matrizMelhorJogadaMedia()
          melhorJogada[8,1] <- "11"
          melhorJogada[8,2] <- "33"
          melhorJogada[8,3] <- "13"
          melhorJogada[8,4] <- "12"
          
          melhorJogada[9,1] <- "11"
          melhorJogada[9,2] <- "33"
          melhorJogada[9,3] <- "13"
          melhorJogada[9,4] <- "23"

          melhorJogada[10,1] <- "11"
          melhorJogada[10,2] <- "33"
          melhorJogada[10,3] <- "31"
          melhorJogada[10,4] <- "32"

          melhorJogada[11,1] <- "11"
          melhorJogada[11,2] <- "33"
          melhorJogada[11,3] <- "13"
          melhorJogada[11,4] <- "21"
fimprocedimento
//INICIALIZAR VARIAVEIS NECESSÁRIAS ///////////////////////////////////
procedimento iniciaVariaveisNecessarias()
   var
   inicio
      COMPUTADOR      <- "COMPUTADOR"
      ADVERSARIO      <- "ADVERSARIO"
      permitirEmpate  <- falso
      pecaVazia       <- "                            "
      melhoresJogadas <- 150
      indiceJogadores <- 1
      textoVazio      <- "VAZIO"
      textoX          <- "X"
      textoO          <- "O"
      rotina          <- 0
      se (randi(2) = 0) entao
         iniciaComputador <- verdadeiro
      senao
         iniciaComputador <- falso
      fimse
      para i de 1 ate 150 faca
         para j de 1 ate 5 faca
            melhorJogada[i, j] <- " "
         fimpara
      fimpara
   fimprocedimento
///////////////////////////////////////////////////////////////////////
Var
   // Seção de Declarações das variáveis
   tela:   vetor[1..12] de caracter
   pecaX:  vetor[1..9 ] de caracter
   pecaO:  vetor[1..9 ] de caracter
   jogadas: vetor[1..5] de caracter
   vetorX: vetor[1..5] de caracter
   vetorO: vetor[1..5] de caracter
   melhorJogada: vetor[1..150,1..5] de caracter
   player1 : vetor[1..3] de caracter
   player2: vetor[1..3] de caracter
   alfabeto: vetor[1..27,1..9] de caracter
   Jogadores: vetor[1..150,1..4] de caracter
   jogoVelha:  vetor[1..3, 1..3] de caracter


   auxO, auxX, ultimaMelhorJogada, melhoresJogadas: inteiro
   idJogador1, idJogador2, indiceJogadores, pontosComp, pontosAdv: inteiro
   linhaInicial, linhaMelhor, colunaMelhor, linhaEstatica, linhaJogadas: inteiro
   comp, p, cont, i, j, rodada, rotina: inteiro
   jogador, continuar, tipoJogo, jogoComputador: caracter
   pecaVazia, pecaComputador, pecaAdversario, textoVazio, textoX, textoO: caracter
   COMPUTADOR, ADVERSARIO, vencedor: caracter
   permitirEmpate, iniciaComputador, cadastrado: logico
   equipeOuIndividual: caracter
Inicio
////////////////////////////////////////////////////////////////////
//      INICIALIZAR FRONT -END            //////////////////////////
   para i de 1 ate 12 faca                  ////////////////////////
      leia(tela[i])                         ////////////////////////
   fimpara                                  ////////////////////////
   para i de 1 ate 9 faca                   ////////////////////////
      leia(pecaX[i])                        ////////////////////////
   fimpara                                  ////////////////////////
   para i de 1 ate 9 faca                   ////////////////////////
      leia(pecaO[i])                        ////////////////////////
   fimpara                                  ////////////////////////
   para i de 1 ate 27 faca                  ////////////////////////
      para j de 1 ate 9 faca                ////////////////////////
         leia(alfabeto[i,j])                ////////////////////////
      fimpara                               ////////////////////////
   fimpara                                  ////////////////////////
   limpatela()                              ////////////////////////
////////////////////////////////////////////////////////////////////
///////////    BACK-END    ////////////////////////////////////////////
//      ALGORITMO DO JOGO      ////////////////////////////////////////

   
   iniciaVariaveisNecessarias()
   mudacor("verde", "fundos")
   painelInicial()
   nivelJogo()
   zerarJogo()
   escolheJogo()
   repita
      se jogoComputador = COMPUTADOR entao
         recebeJogadas()
      senao
         tela()
         recebeJogadas()
      fimse
      se (rodada = 10) e (haVencedor = falso) entao
         mudacor("vermelho","fundos")
         tela()
         pularLinha(1)
         apresentarMensagem("         DEU VELHA         ")
         se permitirEmpate entao
            incluirPontuacao(idJogador1,1)//Passa o ID do vencedor e apontuação
            se tipoJogo = ADVERSARIO entao
               incluirPontuacao(idJogador2,1)//Passa o ID do vencedor e apontuação
            fimse
         fimse
         pularLinha(1)
         escreval("VER RANKING [ APERTE ENTER ]")
         leia(continuar)
         montarRanking()
      fimse
   ate rodada = 10
Fimalgoritmo
