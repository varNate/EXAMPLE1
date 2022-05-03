#Python 3.10


#Booleani
Gelateria_Aperta = True

#Dichiarazione Varianti
drink_alcolici = ["Aperol Spritz", "Long Island", "Negroni", "Angelo Azzurro", "4 Bianchi"]
gelato_speciale = "Tartufo di Pizzo Calabro."
prezzo_gelato_speciale = 14.50 
nome_barman = "Laura"
sconto =  3
gelati = ["Cioccolato","Fragola","Mango","Setteveli","Nocciola","Fior di latte","Stracciatella","Cassata siciliana","Tartufo di Pizzo Calabro"]
gelati.sort ()
#inizio programma
print ("Come ti chiami?")
nome_cliente = input()
print ("Ciao "+str(nome_cliente))
print ("\nBenvenuto nella gelateria artigianale il tartufo d'oro!")
print ("Mi chiamo "+nome_barman+".. E sono pronta a servirti!")
print ("\nil gelato piu apprezzato della nostra gelateria è il "+str(gelato_speciale))
print ("Provalo Subito, a soli "+str(prezzo_gelato_speciale))
print ("\nInserci il tuo anno di nascità.")

anno_nascita = int(input())
anni_cliente = 2022 - anno_nascita

print ("Hai "+str(anni_cliente)+" anni")

if anni_cliente < 18:
    print ("\nCi dispiace, sei minorenne quindi potrai ordinare solo drink analcolici e gelati")
elif anni_cliente > 40:
    print("\nWOW! abbiamo delle promozioni sui gelati per te!")

else:
    anni_cliente > 18
    print ("\nSei maggiorenne! puoi ordinare qualsiasi cosa tu voglia!")

print ("\nQuesti sono i nostri gelati\n")

while  True:
#Variabile di ciclo
    for gelato in gelati:
           print (gelato)
                  
    if anni_cliente > 18:
        print ("\nLista dei nostri drink\n")
        print (drink_alcolici[0])
        print (drink_alcolici[1])
        print (drink_alcolici[2])
        print (drink_alcolici[3])
        print (drink_alcolici[4])

    prodotti = drink_alcolici+gelati

    prodotto_scelto = input()
    if prodotto_scelto in prodotti:
         print("\nHai scelto "+prodotto_scelto+". Goditelo!")
         break
    else:
        print("\nIl prodotto scelto ci risulta essere  non disponibile. Scegli  un altro prodotto!\n")



