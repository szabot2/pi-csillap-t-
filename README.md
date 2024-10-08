## &#928; Csillapító Áramkör Jegyzőkönyv.

**Mérés helye**: Miskolci SZC Kandó Kálmán Informatikai Technikum  
**Mérés időpontja**: 2024.10.07.  
**Mérő műszerek**: HMO1002 Oscilloscope - 1764K02-102609-WG  
**Felelős személy**: Sándor Péter  
**Cél**: A pi csillapító áramkör elemzése.

---

### 1. **Bevezetés**

A projekt célja egy PI csillapító áramkör megépítése, amelynek fókuszában a csillapítás mérése áll.
Az áramkört breadboardon építettem meg, a könnyedség kedvéért.

## Elmélet:

Az áramkör arról kapja a nevét, hogy az ellenállásokat a görög "&#928;" formájában kötjük össze.
Az érétkeket a következő képletekkel számoljuk ki:

![R1 képlete](https://raw.githubusercontent.com/szabot2/pi-csillapito/cffee4ced185268076fb4bf54fdfafc23a0b0f74/kepek/svgviewer-output.svg)

![R2 képlete](https://raw.githubusercontent.com/szabot2/pi-csillapito/cffee4ced185268076fb4bf54fdfafc23a0b0f74/kepek/svgviewer-output(1).svg)


6 dB-es csillapításra kiszámolt ellenállás értékek:


<img src="https://raw.githubusercontent.com/szabot2/pi-csillapito/refs/heads/main/kepek/ql_41d4e91c270a0827beb0bb25f1c6a62a_l3.png">
<br>

A kapcsolási rajz ábrázolja a jelgenerátort a belső ellenállásával, valamint a Pi csillapítót a kiszámolt ellenállás értékekkel:
<img src="https://raw.githubusercontent.com/szabot2/pi-csillapito/refs/heads/main/kepek/circuit-20241007-1359(1).png" width="600" height="480">

### 3. **Mérési paraméterek**

| Paraméter           | Érték |
|---------------------|-------|
| Generátor jel       | 5.00 Vpk|
| Kimeneti Jel        | 2.06 Vpk |
| Generátor Frekvencia| 1000 Hz |
| Csillapítás         | -7.702 dB |
| Átviteli Arány      | 7.702 dB |
| Bemeneti impedancia | ? Ω |
| Kimeneti impedancia | ? Ω |   

<br>

Látható az oszcilloszkópon a sárga 1-es csatornán a csillapított kimeneti jel, és a kék 2-es csatornán a generátor jel.

<img src="https://raw.githubusercontent.com/szabot2/pi-csillapito/refs/heads/main/kepek/TA02.PNG" width="600" height="480">


### 4. **Mérési eredmények**

- **Kimeneti Jel**: A kimeneti jel mindössze 41.2%-a a generátor jelének.
  
- **Csillapítás/Átviteli arány**:  7.702 dB csillapítást tapasztalunk az áramkör jóvoltából.

- **Kimeneti/Bemeneti impedancia**: ??????.  

### 5. **Elemzés**
A pi csillapító (pi pad) ellenállás áramkörének elemzése során megfigyelhető, hogy a tervezett áramkör hatékonyan csökkenti a jel amplitúdóját, miközben megőrzi a jel formáját. Az áramkör négy fő komponensből áll: három ellenállásból és egy terhelő ellenállásból. Kisebb eltérés tapasztalható a kiszámolt értékek és a valós értékek között.

### 6. **Következtetések**
A pi csillapító áramkör sikeresen megvalósult, és a tesztelési eredmények azt mutatják, hogy a csillapítási teljesítmény megfelel a tervezett specifikációknak. A mérések alapján a csillapító hatás a kívánt frekvenciatartományban optimális, és a jelminőség megőrzése is megfelelő. A projekt során szerzett tapasztalatok alapján a tervezési folyamat során figyelembe kell venni a komponensek toleranciáját és a környezeti hatásokat, mivel ezek befolyásolhatják az áramkör teljesítményét.

### 7. **Javaslatok**

- nincs

---

**Aláírás**:  
Felelős mérő személy: ..............................  
Dátum: .............................................
