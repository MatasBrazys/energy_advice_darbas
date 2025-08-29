#Uzdavinys 2

Šiame projekte sukurtas neuroninis tinklas, kuris rekomenduoja įėjimo signalą x , kad sistemos išėjimas y išlaikytų pastovią reikšmę.

Duota sistema:
y(i) = y(i-1) + 0.01y(i-2) + 8x(i-1) - 0.3x(i-2) + 0.1z(i-1)
z(i) = z(i-1) + 2*x(i-1) + 0.11

Kur:
- x – valdymo signalas,
- y – sistemos išėjimas,
- z – papildoma būsena.

#Uzduotis:

Neuroninis tinklas apmokomas parinkti x, kad:
- y būtų artimas pastoviai reikšmei (y*).
- Demonstracijoje iki i = 200 turime y* = 5, o nuo i = 200 – y* = 7.

#NAUDOJIMAS:
1. Įsidiekite priklausomybes
pip install -r requirements.txt

2. Paleiskite uzd2.ipynb
   -(Aš naudojau notebooką conda bash ir jupyter lab'o aplinkoje.)

3. Įvykdykite visą kodą iš eilės.
   (galimas ir netreniruoti, nes palikau ištreniruotą modelį, tačiau treniravimas labai neilgas ypac su tensorflow gpu ~10s)

#Parametrai

Notebook'e galima keisti:
  y1, y2 – norimos y reikšmės (pvz. 5 → 7).
  switch_i – žingsnis, kuriame keičiasi y*.
  clip_x – ribojimas valdymo signalui x. 
  Treniruotės parametrus (epochs, batch_size, paslėptų sluoksnių dydį).

#Rezultatai

Notebook sugeneruoja 3 grafikus: 
  y vs y* – kaip tiksliai tinklas seka norimą reikšmę.
  x – valdymo signalo dinamika.
  z – papildomos būsenos dinamika.
