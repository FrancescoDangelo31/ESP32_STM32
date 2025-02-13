# ESP32_STM32
In questa repository sono presenti i file che abbiamo utilizzato per la realizzazione della tesina di laboratorio di automazione.

Sono presenti sia i file STM32 per la scheda STM32745_ZQI, sia quelli per la scheda STM32755_ZQI, sono programmi molto semplici che
sfruttano la trasmissione e la ricezione dei dati. Dunque fare il porting dei codici da una scheda all'altra è molto semplice.
Perche al livello di IOC , semplicemente nei programmi base è abilitata una USART , in quello finale una USART2 in interrupt mode e 
una usart3 che iin realtà la utilizziamo solo per debuggare i codici e capire cosa arriva alla scheda stm32 ad esempio tramite putty.
Dunque basta avere il file con abilitate queste due cose e banalmente il codice principale in USER CODE può essere preso da una scheda
all'altra. Questo lo abbiamo già fatto noi. e siamo sicuri che i codici funzionano tutti quanti sia per la 745 che per la 755 (in vista
del fatto che il corso si sposterà in direzione 755 data la scarsa reperibilità della vecchia scheda).

Durante il corso abbiamo inoltre approfondito questo aspetto e abbiamo ottenuto risultati pressocchè identici.

Le informazioni tecniche per quanto riguarda cosa cambia da una scheda all'altra possono essere trovati online.
Per la nostra esperienza , quello da tenere in conto è stato riportato nella tesina e banalmente lo ricordiamo ance qui:

-Risolto overcloking nella 755 ( dunque in alcuni esercizi del corso bisogna tenere a mente di fare i calcoli per conto proprio 
quanto si usa la 755, ovvero per prescaler e counter period.

-La parte di codice da aggiungere per il debugging sul CM7 è identico, questa porzione di codice va aggiunta se si vuole fare un debugging 
profondo del programma


