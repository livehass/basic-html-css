```css
/*importa as fontes */
@import url('https://fonts.googleapis.com/css2?family=Krona+One&family=Montserrat:wght@400;600&display=swap');
        :root{
            --default-black: #002B5B;              /*variaveis de cores e fonte*/
            --default-white: #F9F5EB;
            --default-blue:  #EA5455; 
            --default-hover: #414141;
            --default-font:  'Krona One', sans-serif;   
            --second-font:   'Montserrat', sans-serif;
        }
        *{
            margin: 0;
            padding: 0;                             /*reset da margin e do padding para iniciar*/            
        }
        body {
            /*retiramos o tamanho que seria sempre 100% do viewport por que adicionamos um rodapé*/
            /*height: 100vh;                         definimos o tamanho do body para 100% do tamanho da viewport*/
            box-sizing: border-box;                  /*garantimos que os filhos do body não vao sair de dentro dele*/
            background-color: var(--default-black);  /*cor de fundo do body*/
            color: var(--default-white);             /*cores das letras principais do body*/
        }
        .cabecalho{                                 /*sequencia de um padding*/ 
                                                    /*cima, direita, abaixo, esquerda*/
            padding: 2% 0% 0% 15% ;                 /*padding apenas em cima e a esquerda*/
        }
        .cabecalho__menu {
            display: flex;                          /*inicia o display flex, para usar flexbox*/
            gap: 80px;
        }
        .cabecalho__menu__link {
            font-family: var(--second-font);         /*fonte*/
            font-weight: 600;                       /*peso*/
            font-size: 24px;                        /*tamanho*/
            color: var(--default-blue);             /*cor dos itens do navbar*/
            text-decoration: none;                  /*removemos a decoração padrao do texto*/
        }
        .apresentacao{
            /*margin: 10% 15%;                      os vão ter uma margem na lateral*/
            padding: 5% 15%;                        /*vamos ultilizar o padding no lugar do margin para colocarmos a nav bar*/
            display: flex;                          /*os itens vão ficar alinhados*/
            align-items: center;                    /*os itens se alinham ao centro da tela*/
            justify-content: space-between;         /*cria uma espaçamento entre os itens*/
            
        }
        .apresentacao__conteudo {
            width: 615px;                           /*tamanho do conteudo pego no figma*/
            display: flex;                          /*adicionamos o display flex para mudarmos o flex direction*/
            flex-direction: column;                 /*o flex tem como parametro padrao a vertical, mudamos agora para coluna*/
            gap: 40px;                              /*espaçamento entre os conteudos da section*/
        }
        .apresentacao__conteudo__titulo {
            font-size: 36px;                        /*tamanho da fonte*/
            font-family: var(--default-font)        /*fonte*/
           
        }
        .destaque{
            color: var(--default-blue);             /*cor da strong em destaque*/
        }
        .apresentacao__conteudo__paragrafo {
            font-size: 24px;                        /*tamanho da fonte*/
            font-family: var(--second-font);         /*fonte*/
        }
        .apresentacao__links{
            display: flex;                          /*sempre que vamos mexer no espaço colocamos no pai o display flex*/
            justify-content: space-between;         /*espaçamento entre os itens*/
            flex-direction: column;                 /*alinhamento dos itens em coluna*/
            align-items: center;                    /*alinha os itens no centro*/          
            gap: 32px;                              /*adiciona um espaçamento entre os itens*/
        }
        .apresentacao__links__subtitulo{
            font-family: var(--default-font);       /*fonte*/
            font-weight: 400;                       /*peso da fonte*/
            font-size: 24px;                        /*tamanho da fonte*/
        }
        .apresentacao__links__link{
         /* background-color: var(--dfefalt-blue);  cor de fundo da ancora */
            display: flex;                          /*voltamos para o posicionamento padrao*/
            justify-content: center;                /*o conteudo vao para o centro*/
            width: 378px;                           /*tamanho do botão pego no figma*/
            text-align: center;                     /*alinha os textos ao centro*/
            border-radius: 8px;                     /*raio da borda*/
            font-size: 24px;                        /*tamanho da fonte*/
            font-weight: 600;                       /*fonte em negrito como do figma*/
            padding: 21.5px 0;                      /*espaçamento entre a borda e o item*/
            text-decoration: none;                  /*tira a rasura do texto*/
            color: var(--default-white);            /*cor do texto*/
            font-family: var(--second-font);  /*fonte*/
            border: 2px solid var(--default-blue);  /*borda solida de 2px cor azul*/
            gap: 16px;                              /*espaçamento interno 16px*/
        }
        .apresentacao__links__link:hover{
            background-color: var(--default-hover); /*passando o mouse por cima*/
        }
        .apresentacao__imagem {                     /*imagem ultilizara 50% do elemento pai*/
            width: 50%;                             /*nesse caso a main apresentacao*/
        }                                           /*parte  de deixar o site responsivo*/
                                                    /*com tamanhos de acordo com cada browser*/
        .rodape{
            font-family: var(--second-font);        /*fonte*/
            font-weight: 400;                       /*peso da fonte*/
            font-size: 24px;                        /*tamanho da fonte*/
            padding: 24px;                          /*espaçamento entre o item e a borda */
            color: var(--default-black);            /*cor texto preto*/
            background-color: var(--default-blue);  /*cor de fundo*/
            text-align: center;                     /*alinhar o texto no centro*/
        }
        /*todos os parametros do font-size mudaram para 1.5rem tamanho relativo ao tamanho raiz do html, o tamanho root ou seja o tamanho que o usuario ultiliza em seu browser*/
      
@media (max-width: 1200px){ /*media querie, quando a tela for menor que 1200px*/
            .apresentacao {
               flex-direction: column-reverse;        /*todo o conteudo da main fica em coluna*/  
            }                                         /*column-reverse reverte a ordem que os itens aparecem na coluna*/
        }  

        