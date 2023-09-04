# Introdução

## 1 - Um pouco de história sobre computação e eletrônica
    * Começo na Babilonia em 2400 a.C, uso do abaco.
    * Entre 200 a.C. e 400, os indianos, inventaram logarítimo
    * Entre (1592-1635), Wilhelm Schickard construíu a primeira calculadora
    * Entre (1792-1871), Charles Babbage desenvolver máquina para realizar máquina para cálcular polinômios
    * Em 1854, George Boole publica álgebra booleana
    * Nasce primeiro computador, chamado de Z1, o alemão Konrad Zuse (1910-1995) construiu a parir de relé que efetuada cálculo. Em seguida os americanos desenvolveram o ENIAC em 1946
    * Durante 2 guerra mundial Alan Turing constroí a Máquina de Turing (Nascimento da Ciência da Computação)
    * John Von Neumann (1903-1957) formalizou o projeto lógico de um computador
    * Entre 1950 e 1960, EUA e Europa concorre na invenção do Transitor

## 2 - Sistema númerico
    decimal     = 10
    hexdecimal  = 16
    nossa       = 5
    octadecimal = 8
    binario     = 2

    * Decimal
        Digitos: 
            0 1 2 3 4 5 6 7 8 9

        Formação:
            42 => 4x10^1 + 2x10^0 = 42

                            4 2 => 4 x 10^1 + 2 x 10^0 =  4x10 + 2x1 = 40 + 2 = 42
            (index) posicao 1 0

                            2 2  => 2 x 10^1 + 2 x 10^0 = 20 + 2 = 22
                            1 0

                            2 0   => 2 x 5^1 + 2 x 5^0 = 10 + 2 = 12
                            1 0

        Para binário:
            42 / 2 (base) => 21                            resto é igual a 42 - 21 * 2  = 0
            21 / 2 =>        10 (só pega parte inteira)    resto é igual a 21 - 10 * 2  = 1
            10 / 2 =>        5                             resto é igual a 10 -  5 * 2  = 0
            5  / 2 =>        2                             resto é igual a  5 -  2 * 2  = 1
            2  / 2 =>        1                             resto é igual a  2 -  1 * 2  = 0
            1  / 2 =>        0                             resto é igual a  1 -  0 * 2  = 1

        Lendo debaixo pra cima fica: 101010
        
    * Binario
        Digitos: 0 ou 1 (true/false ou ligado/desligado ou low/high)
        Formação:
            0 ou 1
        Para decimal
            0x2^6 + 1x2^5 + 0x2^4 + 1x2^3 + 0x2^2 + 1x2^1 + 0x2^0 => 0 + 32 + 0 + 8 + 2 + 0 => 42

            1 0 1 0 (binario)
            3 2 1 0 (posicao)

            1x2^3 + 0x2^2 + 1x2^1 + 0x2^0 = 1x8 + 0x4 + 1x2 + 0 = 8 + 0 + 2 + 0 = 10

            da base menor para maior (divide)
            da maior para menor (mutiplica)

    * Hexadecial
        Digitos:
            0 1 2 3 4 5 6 7 8 9 A  B  C  D  E   F
                                10 11 12 13 14 15

        Formação:
            2A => 2x16^1 + Ax16^0 = 32 + 11 = 42

                  2x16^1 + Ax16^0 = 32 + A = 32 + 10 = 42    

          2    A
          0010 1010

        De decimal para hexa:
            42 / 16 = 2 resto 10 -> A
            2 / 16 =  0 resto 2  -> 2
            
        Lendo debaixo pra cima fica: 2A

        F =>    1111
        FF      1111 1111
        FFFF    1111 1111 1111 1111
        FFFFFFFF  (1111 1111) (1111 1111) (1111 1111) (1111 1111) = (4 bytes)
      
        bit      = 1 ou 0
        byte     = 8 bits

## 3 - Curiosidades
    * Tabela ASCII possuí 256 caracter, cada caracter é representado por 1 byte ou 8 bits, peceba que 2^8 gera 256 possiveis valores.
    * Cada letra em hexadecimal corresponde a 1 byte (8 bits) então:
     a) FF               -> 1111 1111                                                                                  (1 bytes)  (8 bits)
     b) FFFF             -> 1111 1111 1111 1111                                                                        (2 bytes)  (16 bits)
     c) FFFFFFFF         -> 1111 1111 1111 1111 1111 1111 1111 1111                                                    (4 bytes)  (32 bits)
     d) FFFFFFFFFFFFFFFF -> 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111 1111            (8 bytes)  (64 bits)
    * Cores no css/html, usamos 6 bytes em hexadecimal, ou FF FF FF, ou 16777215 decimal

## 4 - Eletrônica
    * Digital e Analogica
    * Analógica
        - Registores, diodos, capacitores, bobinas, transitors, potênciometro, cristais, sensores
        - Transitors, existe duas categorias:
            PNP -> P (positivo) - N (negativo) - P (positivo)
            NPN -> N (negativo) - P (positivo) - P (positivo)
    * Digital:
        - CI (Circuito integrado)
