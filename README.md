# atv.02
logica d programação
lgoritmo "Shoping de carros
// Disciplina   : [Linguagem e Lógica de Programação]
// Descrição   : 
// Autor(a)    : Miquel Alves
// Data atual  : 18/05/2023
Var
   // Seção de Declarações das variáveis
   LOGIN: CARACTERE
   SENHA: INTEIRO
   INFORMADOLOGIN: CARACTERE
   INFORMADOSENHA: INTEIRO

   //INICIO DECLARACOES DE VARIAVEIS PARA CADASTRO DE VEICULOS
   OBJETO1, OBJETO2, OBJETO3, OBJETO4, OBJETO5, OBJETO6: CARACTERE
   OBJETO7, OBJETO8, OBJETO9, OBJETO10: CARACTERE
   // FIM DAS VARIAVEIS UTILIZADAS PARA CADASTRO DE VEICULOS

   //INICIO DE VARIAVEIS GLOBAIS
   ACESSO:INTEIRO
   ACESSO2: INTEIRO
   //FIM VARIAVEIS GLOBAIS

   //VARIAVEIS PARA CADASTRO VEICULOS PELO O OPERADOR DO SISTEMA

   VEICULO, VENDA, CARACTERISTICAS, ANO: INTEIRO
   VALOR:REAL
   // FIM DAS VARIAVEIS UTILIZADAS PELO OPERADOR DO SISTEMA

   PAG: REAL

   SILVIO,TROCO,VLRCL,VLRV:REAL

   VALORPARCELA, VLRVCARD,QUANTPARCELAS: REAL
   // INICIO VARIAVEIS DO FINANCIAMENTO
   ESCFINAN, VLRFINAN, PARCFINAN, JUROS: REAL
   //FIM VARIAVEIS FINANCIMANTO


Inicio
   // Seção de Comandos PARA LOGIN E SENHA
   LOGIN <- "LCC"
   SENHA <-2535
   REPITA
      ESCREVAL ("SEJA BEM VINDO AO SHOPING CAR")
      ESCREVAL ("LOGIN")
      LEIA(INFORMADOLOGIN)
      ESCREVAL("SENHA")
      LEIA (INFORMADOSENHA)

      SE (INFORMADOLOGIN = LOGIN ) E (INFORMADOSENHA = SENHA) ENTAO
         ESCREVAL("OLA, SEJA BEM VINDO")
      FIMSE
   ATE (INFORMADOLOGIN = LOGIN ) E (INFORMADOSENHA = SENHA)





   // FIM de Comandos PARA LOGIN E SENHA


   // INICIO DE CADASTRO DE VEICULOS
   OBJETO3 <- "01 HILUX ANO 2022,CABINE DUPLA, COR: PRETA, VALOR R$230.000,00"
   OBJETO4 <- "02 HILUX ANO 2023,CABINE ESTENDIDA, COR: PRETA, VALOR R$330.000,00"
   OBJETO5 <- "03 HILUX ANO 2023,CABINE DUPLA, COR: PRETA, VALOR R$340.000,00"
   OBJETO6 <- "05 HILUX ANO 2022,CABINE DUPLA, COR: VERMELHA, VALOR R$300.000,00"
   OBJETO7 <- "06 COROLLA ANO 2022,BLINDADO, COR: VERMELHA, VALOR R$120.000,00"
   OBJETO8 <- "07 COROLLA ANO 2023,HIBRIDO, COR: VERMELHA, VALOR R$300.000,00"
   OBJETO9 <- "08 COROLLA ANO 2018,SERIE ADVENTURE, COR: VERMELHA, VALOR R$80.000,00"
   OBJETO10 <- "09 COROLLA,ANO 2020, COR: VERMELHA, VALOR R$100.000,00"
   // FIM DE CADASTRO DE VEICULOS




   // INICIO de Comandos OPERACOES DO SISTEMA
   REPITA
      ESCREVAL("DIGITE 01 PARA CONSULTAR VEICULOS")
      ESCREVAL("DIGITE 02 PARA CADASTRAR VEICULOS")
      ESCREVAL("DIGITE 03 PARA VENDER VEICULOS")
      ESCREVAL("DIGITE 10 PARA SAIR")
      LEIA(ACESSO)

      SE ACESSO = 1 ENTAO
         ESCREVAL(OBJETO3)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO4)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO5)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO6)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO7)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO8)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO9)
         ESCREVAL("____________________")
         ESCREVAL(OBJETO10)
         ESCREVAL("***********************************")

      SENAO

         SE ACESSO = 2 ENTAO


            ESCREVAL("INFORME O NOME DO VEICULOS")
            LEIA(VEICULO)
            ESCREVAL("INFORME O ANO DO VEICULO")
            LEIA(ANO)
            ESCREVAL("INFORME O CARACTERISTICAS DO VEICLO")
            LEIA(CARACTERISTICAS)
            ESCREVAL("INFORME O  VALOR DO VEICULOS")
            LEIA(VALOR)
            ESCREVAL("******************")
            ESCREVAL("VEICULO CADASTRADO")
            ESCREVAL("VEICULO", VEICULO)
            ESCREVAL("ANO", ANO)
            ESCREVAL("CARACTERISTICAS", CARACTERISTICAS)
            ESCREVAL("VALOR", VALOR)
            ESCREVAL(" ***********************************")



         SENAO
            SE ACESSO = 3 ENTAO
               //EM CONSTRUCAO
               ESCREVAL("DIGITE 01 PARA PAGAMENTO A VISTA")
               ESCREVAL("DIGITE 02 CARTAO DE CREDITO OU DEBITO")
               ESCREVAL("DIGITE 03 FINANCIAMENTO")
               ESCREVAL("DIGITE 10 PARA SAIR")
               LEIA(PAG)

               SE PAG = 1 ENTAO

                  ESCREVAL("INFORME O VALOR DO VEICULO")
                  LEIA(VLRV)

                  ESCREVAL("INFORME VALOR RECEBIDO PELO CLIENTE")
                  LEIA( VLRCL)

                  TROCO<-(VLRCL-VLRV)

                  ESCREVAL("VEICULO PAGO")
                  ESCREVAL("TROCO",TROCO)
               SENAO
                  SE PAG =2 ENTAO

                     ESCREVAL("INFORME O VALOR DO VEICULO")
                     LEIA(VLRVCARD)

                     ESCREVAL("INFORME A QUANTIDADE DE PARCELAS")
                     LEIA( QUANTPARCELAS)


                     VALORPARCELA <-( VLRVCARD / QUANTPARCELAS)

                     ESCREVAL("VALOR DA SUA PARCELA E", VALORPARCELA )
                  SENAO

                     //INICIO DA TERCEIRA PARTE DA VENDA (FINANCIAMENTO)
                     SE PAG =3 ENTAO
                        ESCREVAL("INFORME O VALOR DO VEICULO")
                        LEIA(VLRFINAN)

                        ESCREVAL("ESCOLHA A QUANTIDADE DE PARCELAS PARA O SEU FINANCIMANTO")
                        ESCREVAL("36X ---- DIGITE 36")
                        ESCREVAL("48X -----DIGITE 48")
                        ESCREVAL("60X -----DIGITE 60")
                        LEIA(ESCFINAN)
                        SE ESCFINAN = 36 ENTAO
                         JUROS <-  (VLRFINAN*0.04)
                           PARCFINAN <- (VLRFINAN/36) + JUROS
                           ESCREVAL (" VOCE PARCELOU EM 36X, O VALOR DA SUA PARCELE E:",PARCFINAN)
                           ESCREVAL ("PARABENS SEU SONHO VAI FAZER VC PAGAR DUAS VEZES O VALOR REAL DO BEM ADQUIRIDO")
                           ESCREVAL ("OTARIO VAI PAGAR APENAS",PARCFINAN*36)
                        SENAO
                           SE  ESCFINAN = 48 ENTAO
                               JUROS <-  (VLRFINAN*0.04)
                              PARCFINAN <- (VLRFINAN/36)+JUROS
                              ESCREVAL (" VOCE PARCELOU EM 48X, O VALOR DA SUA PARCELE E:",PARCFINAN)
                              ESCREVAL ("PARABENS SEU SONHO VAI FAZER VC PAGAR DUAS VEZES O VALOR REAL DO BEM ADQUIRIDO")
                              ESCREVAL ("OTARIO VAI PAGAR APENAS",PARCFINAN*48)
                           SENAO

                              SE  ESCFINAN = 60 ENTAO
                                 JUROS <-  (VLRFINAN*0.04)
                                 PARCFINAN <- (VLRFINAN/60)+JUROS
                                 ESCREVAL (" VOCE PARCELOU EM 60X, O VALOR DA SUA PARCELE E:",PARCFINAN)
                                 ESCREVAL ("PARABENS SEU SONHO VAI FAZER VC PAGAR DUAS VEZES O VALOR REAL DO BEM ADQUIRIDO")
                                 ESCREVAL ("OTARIO VAI PAGAR APENAS",PARCFINAN*60)

                              FIMSE
                           FIMSE
                        FIMSE
                     FIMSE
                  FIMSE
               FIMSE
            FIMSE
         FIMSE
      FIMSE
        ATE ACESSO = 10
Fimalgoritmo
