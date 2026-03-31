# ELETTRONICA

# ELETTRONICA

ATTENZIONE: PRIMA DI PROCEDERE CON QUALSIASI OPERAZIONE, LEGGERE ACCURATAMENTE LE AVVERTENZE ELENCATE ALL’INIZIO DI QUESTO DOCUMENTO

## 1 GENERALITÀ DEL CIRCUITO ELETTRICO

La scheda di controllo può essere divisa in due blocchi principali:

*   **Controllore**: gestisce tutte le operazioni della macchina. È formato da una CPU con architettura interna a 32 bit (con al suo interno una memoria flash da 2 MB ed una RAM statica da 64 kB), da una memoria flash seriale da 4 MB e da una SDRAM da 8 MB.
*   **Interfaccia**: ha la funzione di rendere disponibile: sul connettore J11 i segnali per il collegamento all’interfaccia RS232, sui connettori J8 e J10 i segnali per il collegamento all’interfaccia USB, sul connettore J13 i segnali per il collegamento all’interfaccia Ethernet, sul connettore J4 i segnali per il collegamento al cassetto rendiresto e sul connettore J5 i segnali per il collegamento al display esterno.

## 2 TESTINA DI STAMPA

La posizione della testina di stampa, è progettata allo scopo di mantenere la linea degli elementi riscaldanti tangente al rullo di trascinamento della carta. L’uniformità di stampa è ottenuta tramite molle che garantiscono la corretta pressione della testina sulla carta.

La stampa avviene attraverso le seguenti fasi:
*   I segnali di controllo della testina forniscono le informazioni sulla quantità di energia che ciascun elemento riscaldante dovrà generare.
*   L’elemento riscaldante (resistenza) genera calore localizzato in un preciso punto (dot).
*   Il calore generato, trasmesso alla superficie della carta termosensibile, causa la colorazione di quest’ultima.

**SEGNALI DI CONTROLLO DELLA TESTINA DI STAMPA:**
I dati vengono trasferiti alla testina di stampa tramite una seriale sincrona (DATA IN / CLOCK / DATA OUT) in uno Shift Register.
Al completamento della trasmissione dei dati, è necessario attivare il Latch per eseguire la copia dei dati trasferiti verso il registro di riscaldamento. Questo permette di eseguire contemporaneamente la trasmissione e il riscaldamento.
In seguito all’attivazione dei segnali di Strobe i dati memorizzati nel registro di Latch eccitano gli elementi riscaldanti. La temperatura della testina è controllata tramite un termistore.

*(Diagramma a blocchi della testina di stampa con segnali VH, GND, TM, VDD, STB2, STB1, LATCH, DATA IN, CLOCK, DATA OUT, LATCH REGISTER, BIT SHIFT REGISTER)*

## 3 STRUTTURA DISPOSITIVO

*(Diagramma a blocchi che mostra la CPU (FLASH INTERNA 2 MB, RAM INTERNA 128 kB) interconnessa tramite BUS con SDRAM 8 MB e FLASH SPI 8 MB. La CPU è collegata a vari moduli e connettori: DRIVER TAGLIERINA, TESTINA DI STAMPA, CONTROLLORE DI RESET, SENSORI, TASTI, MOTORE PASSO PASSO, DRIVER MOTORE, CONNETTORE INTERFACCIA RS232, TRANSCEIVER RS232, CONNETTORE INTERFACCIA ETHERNET, TRANSCEIVER ETHERNET, CONNETTORE INTERFACCIA USB HOST, CONNETTORE INTERFACCIA USB DEVICE, MEMORIA PERMANENTE DI RIEPILOGO, MEMORIA PERMANENTE DI DETTAGLIO, MICRO SD ESTERNA, CONNETTORE CASSETTO RENDIRESTO, CONNETTORE DISPLAY ESTERNO, e un modulo opzionale WI-FI / BLUETOOTH.)*

## 4 SCHEMA INTERCONNESSIONE

*(Diagramma che illustra le interconnessioni tra la SCHEDA DI CONTROLLO e i vari componenti esterni e interni. La SCHEDA DI CONTROLLO (con connettori J13, J10, J4, J22, J23, J24, J7, J16, J15, J2, J26, J11, J5, J8, J27, J18, J19, SW2, SW7, SW1, DL2, SW6) è collegata a:)*
*   **CONNETTORE ETHERNET**
*   **CONNETTORE USB** (due porte)
*   **CONNETTORE SERIALE RS232**
*   **CONNETTORE DISPLAY ESTERNO**
*   **CONNETTORE CASSETTO**
*   **CONNETTORE ALIMENTAZIONE**
*   **MECCANISMO DI STAMPA**
*   **SENSORE QUASI FINE CARTA**
*   **TESTINA DI STAMPA**
*   **TAGLIERINA**
*   **MOTORE / SENSORI MECCANISMO DI STAMPA**
*   **LED DI STATO**
*   **TASTO ON/OFF**
*   **TASTO FEED**
*   **SENSORE FINE CARTA**
*   **SCHEDA MEMORIA PERMANENTE DI RIEPILOGO**
*   **SCHEDA WI-FI / BLUETOOTH** (opzionale, con connettori J1, J3)

## 5 INGRESSI E USCITE SCHEDA DI CONTROLLO DISPOSITIVO

**ALIMENTAZIONE**
Connettore tripolare femmina (J22)

| Pin | Segnale     |
| :-- | :---------- |
| 1   | GND         |
| 2   | +24 Vdc     |
| 3   | GND         |
| 4   | Frame GND   |

L’immagine seguente mostra la piedinatura del connettore del cavo di alimentazione da utilizzare per il dispositivo:
*(Immagine di un connettore tripolare maschio con n.c., +24 V e GND)*

ATTENZIONE:
Rispettare la polarità dell’alimentazione.

**CONNETTORE DISPLAY**
Connettore telefonico femmina (J5)

| Pin | Segnale     | Direzione | Descrizione     |
| :-- | :---------- | :-------- | :-------------- |
| 1   | GND         |           |                 |
| 2   | TX2         | (out)     | Comando display |
| 3   | +24 VT      |           |                 |
| 4   | RX2         | (in)      | Stato display   |

**INTERFACCIA USB**
Connettore USB type A femmina (J10)

| Pin | Segnale     | Direzione |
| :-- | :---------- | :-------- |
| 1   | VBUS-A      | (in)      |
| 2   | HD-         |           |
| 3   | HD+         |           |
| 4   | GND         |           |
| SH1 | GND         |           |
| SH2 | GND         |           |
| SH3 | GND         |           |
| SH4 | GND         |           |

**INTERFACCIA USB**
Connettore USB type B femmina (J8)

| Pin | Segnale     | Direzione |
| :-- | :---------- | :-------- |
| 1   | VBUS-B      | (in)      |
| 2   | DD-         |           |
| 3   | DD+         |           |
| 4   | GND         |           |
| SH1 | GND         |           |
| SH2 | GND         |           |

**INTERFACCIA SERIALE RS232**
Connettore RJ45 femmina (J11)

| Pin | Segnale | Descrizione                                          |
| :-- | :------ | :--------------------------------------------------- |
| 1   | RT1     | Quando è “1”, il dispositivo è pronto per ricevere. |
| 2   | CT1     |                                                      |
| 3   | DTR1    |                                                      |
| 4   | GND     |                                                      |
| 5   | n.c.    |                                                      |
| 6   | RX1     | Durante la ricezione assume i valori “0” e “1” in funzione dei dati. |
| 7   | TX1     | Durante la trasmissione assume i valori “0” e “1” in funzione dei dati. |
| 8   | DTR1    |                                                      |

Poiché siamo in presenza dello standard RS232, al valore logico “0” è associato il valore di tensione +VRS232 (valore di tensione compreso tra +3 Vdc e +15 Vdc) mentre al valore logico “1” è associato il valore di tensione -VRS232 (valore di tensione compreso tra -3 Vdc e -15 Vdc).

**Collegamento DISPOSITIVO > PC**
Nell’immagine seguente è riportato lo schema di un cavo seriale RJ45-DB9 per collegare il dispositivo ad un personal computer (PC) mediante il connettore seriale RS232 a 9 poli:
*(Diagramma di collegamento RJ45 (DISPOSITIVO) a DB9 (PC) con pinout specifici per RTS, CTS, DTR, +VI, RXD, GND, TXD, DCD, RI, DSR)*

Nel caso di utilizzo di un cavo seriale, si consiglia il montaggio di una ferrite sulla parte terminale dello stesso cavo.

**INTERFACCIA ETHERNET**
Connettore RJ45 femmina (J13)

| Pin | Segnale     |
| :-- | :---------- |
| 1   | ETH_RXP     |
| 2   | +3.3VE      |
| 3   | ETH_RXN     |
| 4   | ETH_TXP     |
| 5   | +3.3V       |
| 6   | ETH_TXN     |
| 7   | n.c.        |
| 8   | GND         |
| 9   | +3.3V       |
| 10  | LED_LINK    |
| 11  | +3.3V       |
| 12  | LED-LAN     |
| 13  | SH1         |
| 14  | SH2         |

Le funzioni dei due LED sono indicate nelle seguenti tabelle:

**- Collegamento 10/100Base-TX:**

| LED        | FUNZIONE                                                     |
| :--------- | :----------------------------------------------------------- |
| LED-LNK    | Link: il LED (di colore giallo) si accende quando è attiva una connessione |
| LED-LAN    | Rx/Tx: il LED (di colore verde) si accende quando vengono ricevuti o trasmessi dei dati. |

Il dispositivo riconosce automaticamente il tipo di connessione (cross o pin-to-pin). La piedinatura riportata in tabella è relativa ai segnali in ingresso al componente J13, prima del trasformatore di isolamento (through-hole pin).

**CONNETTORE CASSETTO**
Connettore RJ12 femmina (J4)

| Pin | Segnale |
| :-- | :------ |
| 1   | GND     |
| 2   | CASS1   |
| 3   | IN-CASS |
| 4   | +24VM   |
| 5   | CASS2   |
| 6   | GND     |

Il solenoide del cassetto 1 deve essere collegato dal Pin 2 al Pin 4 del connettore del cassetto.
Il solenoide del cassetto 2 deve essere collegato dal Pin 4 al Pin 5 del connettore del cassetto.
*(Diagramma di collegamento PIN 2, PIN 4, PIN 5 per CASSETTO 1 e CASSETTO 2)*

**Collegamento DISPOSITIVO > CASSETTO RENDIRESTO (opzionale)**
Utilizzare un cavo adattatore RJ12-Jack opzionale per collegare il dispositivo ad un cassetto rendiresto. Per la disposizione dei segnali sui pin, fare riferimento al seguente schema:
*(Diagramma di collegamento RJ12 (DISPOSITIVO) a JACK (CASSETTO RENDIRESTO) con pinout per SOL1, +24Vdc, SOL2)*

**MECCANISMO DI STAMPA** (J23)

| Pin | Segnale   |
| :-- | :-------- |
| 1   | +24VT     |
| 2   | +24VT     |
| 3   | +24VT     |
| 4   | +24VT     |
| 5   | HD-DATA   |
| 6   | DI-DO     |
| 7   | GND       |
| 8   | GND       |
| 9   | GND       |
| 10  | GND       |
| 11  | STB2      |
| 12  | GND       |
| 13  | HD-TEMP   |
| 14  | +3.3V     |
| 15  | HD-LATCH  |
| 16  | HD-SCK    |
| 17  | STB1      |
| 18  | GND       |
| 19  | GND       |
| 20  | GND       |
| 21  | GND       |
| 22  | GND       |
| 23  | DI-DO     |
| 24  | n.c.      |
| 25  | +24VT     |
| 26  | +24VT     |
| 27  | +24VT     |
| 28  | +24VT     |

**MOTORE/SENSORI MECCANISMO DI STAMPA** (J15)

| Pin | Segnale    |
| :-- | :--------- |
| 1   | MOT2B      |
| 2   | MOT1B      |
| 3   | MOT2A      |
| 4   | MOT1A      |
| 5   | VLED-SENS  |
| 6   | PAPER      |
| 7   | GND        |
| 8   | GND        |
| 9   | HEAD-UP    |

**TAGLIERINA** (J16)

| Pin | Segnale   |
| :-- | :-------- |
| 1   | MCUT-     |
| 2   | MCUT+     |
| 3   | SIG-CUT   |
| 4   | GND       |

**SENSORE QUASI FINE CARTA** (J24)

| Pin | Segnale    | Direzione |
| :-- | :--------- | :-------- |
| 1   | VLED-SENS  | (in)      |
| 2   | GND        |           |
| 3   | NPE        |           |
| 4   | +VNPE      |           |

**SCHEDA SENSORE FINE CARTA** (J18)

| Pin | Segnale   |
| :-- | :-------- |
| 1   | +VBM      |
| 2   | NOTCH     |
| 3   | GND       |
| 4   | VLED_BM   |
| 5   | GND       |
| 6   | GND       |

**MEMORIA PERMANENTE DI RIEPILOGO** (J7)

| Pin | Segnale    | Descrizione     |
| :-- | :--------- | :-------------- |
| 1   | GND        |                 |
| 2   | GND        |                 |
| 3   | MF-WE      | Abilita scrittura. |
| 4   | GND        |                 |
| 5   | SSPI7-DI   | Durante l’accesso alla memoria permanente di riepilogo assume i valori 0 V e 3.3 V. |
| 6   | GND        |                 |
| 7   | SSPI7-CSMF | Durante l’accesso alla memoria permanente di riepilogo assume i valori 0 V e 3.3 V. |
| 8   | REG5_3V3   |                 |
| 9   | REG5_3V3   |                 |
| 10  | MF-HOLD    | TTL 3.3V.       |
| 11  | GND        |                 |
| 12  | SSPI7-CK   | Durante l’accesso alla memoria permanente di riepilogo assume i valori 0 V e 3.3 V. |
| 13  | GND        |                 |
| 14  | SSPI7-DO   | Durante l’accesso alla memoria permanente di riepilogo assume i valori 0 V e 3.3 V. |
| 15  | GND        |                 |

**P3-N WI-FI, P3-N BT**

**SCHEDA WI-FI / BLUETOOTH** (J19)

| Pin | Segnale     |
| :-- | :---------- |
| 1   | +3.3V       |
| 2   | GND         |
| 3   | RXD_ESP32   |
| 4   | TXD_ESP32   |
| 5   | CTS_ESP32   |
| 6   | RTS_ESP32   |
| 7   | IRQ_ESP32   |
| 8   | EN_ESP32    |
| SH1 | GND         |
| SH2 | GND         |

**SCHEDA MICRO SD ESTERNA** (J1)

| Pin | Segnale      | Descrizione                                                     |
| :-- | :----------- | :-------------------------------------------------------------- |
| 1   | n.c.         |                                                                 |
| 2   | SPI1-CS-SD1  | Durante l’accesso alla Micro SD card, assume i valori 0 V e 3.3 V. |
| 3   | SPI1-DO      | Durante l’accesso alla Micro SD card, assume i valori 0 V e 3.3 V. |
| 4   | +VFEJ        |                                                                 |
| 5   | SPI1-CK      | Durante l’accesso alla Micro SD card, assume i valori 0 V e 3.3 V. |
| 6   | GND          |                                                                 |
| 7   | SPI1-DI      | Durante l’accesso alla Micro SD card, assume i valori 0 V e 3.3 V. |
| 8   | n.c.         |                                                                 |
| 9   | SD1-IN       | Assume i valori 0 V (Micro SD card inserita) e 3.3 V (Micro SD card non inserita). |
| 10  | GND          |                                                                 |
| 11  | GND          |                                                                 |
| 12  | GND          |                                                                 |
| 13  | GND          |                                                                 |
| 14  | GND          |                                                                 |

## 6 SOSTITUZIONE FUSIBILE

ATTENZIONE:
Prima di effettuare la sostituzione del fusibile accertarsi di avere scollegato il cavo di alimentazione dal dispositivo.

Per accedere al fusibile, che si trova sulla scheda di controllo del dispositivo vicino al connettore di alimentazione, procedere come segue:
*   Smontare il dispositivo seguendo la procedura descritta nella sezione MECCANICA al capitolo 10.
*   Dissaldare il fusibile ai suoi capi, facendo attenzione a non scaldare eccessivamente i componenti vicini, per non danneggiarli.
*   Sostituirlo con un fusibile Bussmann-Eaton cod. 6125TD5-R/TR1 (5 A, 60 Vdc / 125 Vac ritardato) o equivalente.

*(Immagine della SCHEDA DI CONTROLLO con l'indicazione del fusibile F2)*

## 7 LAYOUT SCHEDA DI CONTROLLO

*(Questa sezione presenta due diagrammi del layout della scheda di controllo: "lato componenti" e "lato saldature". I diagrammi mostrano la disposizione dei vari componenti elettronici e le tracce di saldatura sulla scheda. Non è possibile estrarre il testo dettagliato di tutti i componenti e le tracce da queste immagini.)*

## 8 SCHEMI ELETTRICI

*(Questa sezione contiene diversi schemi elettrici dettagliati del dispositivo. Non è possibile estrarre il testo dettagliato di tutti i circuiti e i valori dei componenti da queste immagini, ma si può descrivere il contenuto generale di ciascuna pagina.)*

**Pagina 48:**
*   **Schema principale della CPU**: Mostra le connessioni della CPU (U1A, U1B) con i vari pinout (PDx, PEx, PGx, PAx, PBx, PCx, P6x, P4x, USBx_D+, USBx_D-, P3x, P0x, P1x, P2x, P5x, P7x, P8x, PFx, PJx), alimentazione (VCC, GND, AVCC, AGND, VREFH, VREFL, USB-VCC, USB-GND), e segnali di controllo (RESET, XTAL, EXTAL, EMLE, XCIN, XCOUT, VCL, BSCANP, MD/FINED).
*   **HW CONFIGURATION**: Una tabella con ID0, ID1, ID2 e REVISION.
*   **SDRAM (U29)**: Schema di una SDRAM da 8MBytes con pinout (A0-A12, D0-D15, VSSQ, OE, WE, CAS, VCC, RAS, GND, UDQM, CLK, CKE, BA0, BA1, VDDQ, NC/RFU).
*   **Flash (U7)**: Schema di una memoria Flash da 8MBytes con pinout (CS, S0, WP, SI, VCC, HOLD, SCK, GND).
*   **Shift Registers (U4, U30)**: Schemi di shift register con pinout (D0-D7, Q0-Q7, CLK, OC, VCC, GND).

**Pagina 49:**
*   **DRAWER**: Schema del connettore J4 per il cassetto rendiresto, con pinout (GND, DRW1/TX, SIG1, +VDRW, DRW2, GND) e circuiti di controllo (Q24, Q25, D2, D31, L7, L29, R316, R315, R348, R350, C73, C78, C79, C265).
*   **CUSTOMER DISPLAY**: Schema del connettore J5 per il display esterno, con pinout (GND, TXD(O), PWR(O), RXD(I)) e circuiti di interfaccia RS232 (U3, U16E, U2A, U2B, R28, R31, R32, R33, R342, R351, C71, C72, C74, C75, C76, C77, C264, C217).

**Pagina 50:**
*   **JTAG (RX63N)**: Schema del connettore J6 per JTAG con pinout (TCK, GND, TRST, EMLE, TDO, BSCAN, MD/FIN, +3.3V, TDI, RESET, GND, PC7, TMS, GND) e resistenze/condensatori associati.
*   **EXTERNAL SD CARD (J1)**: Schema del connettore J1 per Micro SD esterna con pinout (CD/DATA3(CS), CMD(DI), VCC, CLK, GND, DAT0(DO), DAT1(RSV), CD-GND, CD, DAT2(NC), FIX1-FIX4) e circuiti di protezione (Q1, R61, C61, C62, R18, R86, C54).
*   **INTERNAL SD CARD (J2)**: Schema del connettore J2 per Micro SD interna con pinout simile a J1 e circuiti di protezione (Q2, R90, R161, R176, R177, C89, C55, C256, C257, L8, R386).
*   **ON BOARD PROGRAMMING (RX63N)**: Connettore J31 con pinout (VBUS, USB_D-, USB_D+, GND, NC, MD/FIN, +3.3V) e resistenze/condensatori associati.
*   **SETUP DIP-SWITCH (SW6)**: Schema del dip-switch SW6 con 10 posizioni e resistenze/condensatori associati.

**Pagina 51:**
*   **USB1 INTERFACE (DEVICE)**: Schema del connettore J10 (USB-A) con pinout (VBUS, DN, DP, GND, SH1-SH4) e circuiti di protezione e interfaccia (U6, U16A, U16F, R73, R76, R77, R116, R117, R374, R394, R395, R398, C65, C111, C115, C116, C117, C119, C171, C309, C315, L10, D35B, D35C, D35A).
*   **USB0 INTERFACE (HOST)**: Schema del connettore J8 (USB-B) con pinout (VBUS, DN, DP, GND, SH1, SH2) e circuiti di protezione e interfaccia (U36, U37, R79, R115, R396, R397, R405, R406, C66, C67, C106, C109, C114, C118, C251, L9).
*   **RS232 INTERFACE**: Schema del connettore J11 (RJ45) con pinout (RTS(O), CTS(I), DTR(O), GND, PWR(O), RXD(I), TXD(O), DTR(O), SH1, SH2) e circuiti di interfaccia (U12, R112, R113, C112, C113, C290, D40).

**Pagina 52:**
*   **ETHERNET INTERFACE (10/100)**: Schema del connettore J13 (RJ45) con pinout (ETH_RXP, +3.3VE, ETH_RXN, ETH_TXP, +3.3V, ETH_TXN, n.c., GND, +3.3V, LED_LINK, +3.3V, LED-LAN, SH1, SH2) e circuiti di interfaccia (U35, U23A, U23B, U23C, U23D, R4, R5, R132, R135, R144, R147, R148, R149, R150, R153, C10, C94, C96, C104, C107, C110, C120, C124, C125, C126, C132, C133, C134, C135, C310, C311, C312, C313, X3). Include anche i LED LINK e ACT.

**Pagina 53:**
*   **PRINTER MECHANISM (OPOS TP347)**: Schemi dettagliati per la testina di stampa, motori/sensori e taglierina.
    *   **PRINTHEAD**: Connettore J23 con pinout (HD-DATA, DI-DO, GND, STB2, HD-TEMP, +3.3V, HD-LATCH, HD-SCK, STB1, GND, DI-DO, +24VT) e circuiti di controllo (U15, R195, R196, R198, R199, R201, C174, C175, C176, C177, L17, L18, L19, L20, D39B, D39C).
    *   **MOTOR/SENSORS**: Connettore J15 con pinout (MOT2B, MOT1B, MOT2A, MOT1A, VLED-SENS, PAPER, GND, HEAD-UP) e circuiti di controllo (U17, R11, R13, R190, R191, R192, R193, R321, R387, R388, C12, C17, C19, C164, C166, C167, C168, C169, C172, C173, C179, C180, C181, C182, D11A, D11B, D11C, D12A, D12B, D13A, D13B, D14A, D14B, L14, L15, L16).
    *   **CUTTER**: Connettore J16 con pinout (MCUT-, MCUT+, SIG-CUT, GND) e circuiti di controllo (Q5, R202, R194, C170, C178).
    *   **PRINTHEAD STROBE CONFIGURATION**: Tabella per la configurazione dello strobe (A, B, NO, YES, HIGH, LOW).

**Pagina 54:**
*   **BATTERY**: Schema della batteria BT2 (3V, 1AH) con diodo D15 e resistenza R221.
*   **ON/OFF SWITCH**: Schema dell'interruttore SW1 con resistenze R234, R220, C51.
*   **FEED SWITCH**: Schema dell'interruttore SW2 con resistenze R230, R223, C52.
*   **STATUS LED**: Schema dei LED (DL2) con resistenze R216, R217, R323, R324, R325, R326, R327, R328, R329, R380, R381, R393, C191, C192, C193, C195, C272, C273, C274, C275, C278, C279, L23, L24, L32, Q6, Q7, Q8, Q9, U18, D36A, D36B.
*   **BUZZER**: Schema del buzzer BZ1 con U34 e resistenze R343, R345, C306.
*   **WI-FI/BLUETOOTH MODULE BOARD**: Connettore J19 con pinout (+3.3V, GND, RXD_ESP32, TXD_ESP32, CTS_ESP32, RTS_ESP32, IRQ_ESP32, EN_ESP32, SH1, SH2).
*   **NEAR PAPER END SENSOR (OUT07)**: Connettore J24 con pinout (VLED, GND, SIGN, +VDD) e resistenze/condensatori.
*   **NOTCH SENSOR/NPE BLACK MARK SENSOR BOARD (ST144-FC1)**: Connettore J18 con pinout (VLED, GND, SIGN, +VDD, SH1, SH2) e resistenze/condensatori.
*   **NOTCH OPTION**: Jumper JP1.

**Pagina 55:**
*   **POWER SUPPLY**: Connettore di alimentazione J22 con pinout (GND, +24V, GND, Frame GND) e circuiti di regolazione (U21, U33, U27A, U27B, U28A, U28B, U22A, U22B, R211, R258, R259, R260, R262, R263, R265, R267, R269, R271, R272, R273, R274, R276, R278, R279, R280, R281, R333, R337, R339, R340, R341, R353, R354, R355, R356, R389, R390, R391, R392, R407, R411, C20, C21, C204, C205, C207, C208, C209, C210, C211, C212, C213, C215, C218, C219, C220, C221, C222, C223, C224, C225, C226, C227, C228, C229, C230, C231, C270, C282, C283, C287, C303, C304, L25, L26, L27, D9A, D9B, D9C, D17, D29A, D29B, D29C, D39A, D39C, Q15, Q16, Q22, Q26, Q28, Q30, F2).
*   **SHIELDED CABLE**: Connettore J26 con pinout (SH1, SH2).
*   **FIDUCIALS MARK**: Punti di riferimento FID1, FID2, FID3.
*   **MOUNTING PADS**: Punti di montaggio.
*   **MECHANICAL HOLES**: Fori meccanici MTH1-MTH12.
*   **GND SHIELD**: Punti di messa a terra.
