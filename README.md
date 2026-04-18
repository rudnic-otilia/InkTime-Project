# InkTime

Smartwatch open-source bazat pe nRF52840, cu display e-paper.

## Diagramă Bloc
<img width="1023" height="752" alt="Diagram" src="https://github.com/user-attachments/assets/fe66f5a5-34c9-4cd6-82d1-0d9e64f8668a" />

## BOM (Bill of Materials)

# Bill of Materials — InkTime

## Componente principale

| Referinta | Componenta | Descriere | Package | Cantitate | JLCPCB / LCSC | Datasheet |
|-----------|-----------|-----------|---------|-----------|---------------|-----------|
| U1 | NRF52840-QIAA-R | MCU principal + BLE 5.0 + USB nativ | aQFN-73 (7×7mm) | 1 | [C190794](https://jlcpcb.com/partdetail/NordicSemicon-NRF52840_QIAAR/C190794) | [Datasheet](https://infocenter.nordicsemi.com/pdf/nRF52840_PS_v1.7.pdf) |
| IC1 | BQ25180YBGR | Charger LiPo cu power-path, I2C | DSBGA-8 (1.6×1.1mm) | 1 | [C3682423](https://jlcpcb.com/partdetail/TexasInstruments-BQ25180YBGR/C3682423) | [Datasheet](https://www.ti.com/lit/ds/symlink/bq25180.pdf) |
| IC9 | RT6160AWSC | Buck-boost regulator 3.3V, I2C | WLCSP-15 (1.4×2.3mm) | 1 | [C7065276](https://jlcpcb.com/partdetail/RichTek-RT6160AWSC/C7065276) | [Datasheet](https://www.richtek.com/assets/product_file/RT6160A/DS6160A-00.pdf) |
| U3 | MAX17048G+T10 | Fuel gauge baterie LiPo, I2C | DFN-8 (2×2mm) | 1 | [C2682616](https://jlcpcb.com/partdetail/MaximIntegrated-MAX17048GT10/C2682616) | [Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/MAX17048-MAX17049.pdf) |
| IC3 | BMA423 | Accelerometru 3-axe + pedometru, I2C | LGA-12 (2×2mm) | 1 | [C189517](https://jlcpcb.com/partdetail/BoschSensortec-BMA423/C189517) | [Datasheet](https://www.lcsc.com/datasheet/C189517.pdf) |
| IC2 | DRV2605YZFR | Haptic driver pentru motor ERM, I2C | DSBGA-9 (1.44×1.44mm) | 1 | [C81079](https://jlcpcb.com/partdetail/TexasInstruments-DRV2605YZFR/C81079) | [Datasheet](https://www.ti.com/lit/ds/symlink/drv2605.pdf) |
| D3 | USBLC6-2SC6Y | Protecție ESD linii USB D+/D- | SOT-23-6 | 1 | [C5310974](https://jlcpcb.com/partdetail/TECHPUBLIC-USBLC62SC6Y/C5310974) | [Datasheet](https://www.st.com/resource/en/datasheet/usblc6-2.pdf) |
| Q3 | SI1308EDL-T1-GE3 | N-channel MOSFET, power gate e-paper | SC-70-3 | 1 | [C10487](https://jlcpcb.com/partdetail/VishayIntertech-SI1308EDLT1GE3/C10487) | [Datasheet](https://www.vishay.com/docs/63587/si1308edl.pdf) |
| Q1 | DMG2305UX-7 | P-channel MOSFET, power switch | SOT-23-3 | 1 | [C252544](https://jlcpcb.com/partdetail/Diodes-DMG2305UXT116/C252544) | [Datasheet](https://www.diodes.com/assets/Datasheets/DMG2305UX.pdf) |
| J4 | KH-TYPE-C-16P | Conector USB-C 16 pini | SMD | 1 | [C2765186](https://jlcpcb.com/partdetail/Kinghelm-KH_TYPEC_16P/C2765186) | [Datasheet](https://www.kinghelm.net/usb-connectors/kh-type-c-16p.html) |
| J1 | 503480-2400 | Conector FPC 0.5mm 24 pini, pentru display e-paper | SMD | 1 | [C262280](https://jlcpcb.com/partdetail/Molex-5034802400/C262280) | [Datasheet](https://www.molex.com/en-us/products/part-detail/503480-2400) |
| J2 | TC2030-IDC | Conector Tag-Connect SWD debug/programare | PCB footprint | 1 | — (hand assembly) | [Datasheet](https://www.tag-connect.com/wp-content/uploads/bsk-pdf-manager/TC2030-IDC_1.pdf) |
| ANT1 | 2450AT18B100E | Antenă chip 2.4GHz pentru BLE | SMD | 1 | [C89771](https://jlcpcb.com/partdetail/Johanson-2450AT18B100E/C89771) | [Datasheet](https://www.johansontechnology.com/datasheets/2450AT18B100E/2450AT18B100E.pdf) |
| X1 | X322516MLB4SI | Crystal HFXO 32MHz, 8pF, ±10ppm pentru nRF52840 | SMD 2016 | 1 | [C13738](https://jlcpcb.com/partdetail/YangxingTech-X322516MLB4SI/C13738) | [Datasheet](https://datasheet.lcsc.com/lcsc/2110221730_YXC-X322516MLB4SI_C13738.pdf) |
| X2 | Q13FC13500004 | Crystal LFXO 32.768kHz, 12.5pF, ±20ppm pentru RTC | SMD 3215 | 1 | [C32346](https://jlcpcb.com/partdetail/Epson-Q13FC13500004/C32346) | [Datasheet](https://www.lcsc.com/datasheet/C32346.pdf) |
| SW_UP, SW_DN, SW_ENT | EVP-AKE31A | Butoane tactile SMD | SMD | 3 | [C3669064](https://jlcpcb.com/partdetail/Panasonic-EVPAKE31A/C3669064) | [Datasheet](https://industrial.panasonic.com/cdbs/www-data/pdf/ATV0000/ATV0000CE5.pdf) |
| D2, D4, D5 | MBR0530 | Diodă Schottky 0.5A 30V, circuit drive e-paper | SOD-123 | 3 | [C424058](https://jlcpcb.com/partdetail/onsemi-MBR0530T1G/C424058) | [Datasheet](https://www.onsemi.com/pdf/datasheet/mbr0530t1-d.pdf) |
| L7 | FTC252012SR47MBCA | Inductor 0.47µH pentru DC/DC | 0402 | 1 | [C408368](https://jlcpcb.com/partdetail/C408368) | — |
| L5 | Inductor 68µH | Inductor boost pentru circuit drive e-paper | SMD | 1 | — (verifică disponibilitate) | — |

---

## Pasive (rezistențe și condensatoare)

| Referință | Valoare | Package | Cantitate | Notă |
|-----------|---------|---------|-----------|------|
| C1, C2, C17, C18 | 12pF | 0201 / 0402 | 4 | Load caps cristale |
| C3, C4 | 1pF | 0201 | 2 | RF matching |
| C5, C7, C8, C12, C19 | 100nF | 0201 / 0402 | 5 | Decoupling MCU |
| C6, C20, C21, C14, C43 | 4.7µF | 0402 | 5 | Bulk decoupling |
| C9 | 820pF | 0201 | 1 | RF matching |
| C11 | 100pF | 0201 | 1 | Decoupling |
| C15 | 1.0µF | 0201 | 1 | Decoupling |
| C16 | 47nF | 0201 | 1 | Decoupling |
| C24, C39 | 10µF | 0402 | 2 | Bulk decoupling |
| C25, C33 | 22µF | 0402 | 2 | Output caps RT6160 |
| C23, C27, C34, C32, C37, C38 | 0.1µF / 1µF | 0201 | 6 | Decoupling PMIC |
| C29, C30, C31, C42 | 1µF / 0.1µF | 0201 | 4 | Decoupling diverși |
| C1-EP-DR | 10µF | 0402 | 1 | Circuit drive EPD |
| C2-EP-DR | 4.7µF/25V | 0402 | 1 | Circuit drive EPD |
| EPD_C1...C12 | 1µF/50V, 0.1µF/50V | 0402 | 10 | Condensatoare display |
| R17, R18 | 3K3 | 0201 | 2 | Pull-up I2C |
| R5, R7, R8, R9, R_PWR_EPD, R2_EP_DR | 10K | 0201 | 6 | Pull-up / bias |
| R1_USB, R2_USB | 5K1 | 0201 | 2 | CC pins USB-C |
| R_TYPE_SEL | 2.2Ω | 0201 | 1 | Selecție tip charger |
| R1_EP_DR | 0.47Ω | 0201 | 1 | Sense rezistor EPD |
| R2, R3, R4 | 0Ω | 0201 | 3 | Jumperi / DNP |
| L1 | 3.9nH | 0201 | 1 | RF matching |
| L2 | 10µH | 0402 | 1 | DC/DC inductor MCU |
| L3 | 15nH | 0402 | 1 | RF matching |

---

# Descriere Hardware

## MCU — nRF52840

Microcontrollerul principal este nRF52840 de la Nordic Semiconductor, un ARM Cortex-M4 la 64 MHz cu BLE 5.0 si USB nativ integrate. Are 1 MB Flash si 256 KB RAM. A fost ales pentru ca include tot ce e necesar intr-un singur chip: procesor, radio BLE si USB, ceea ce simplifica mult designul unui smartwatch.

Are doua cristale externe obligatorii: unul de 32 MHz pentru BLE si USB, si unul de 32.768 kHz pentru ceasul in timp real (RTC) care mentine ora cand dispozitivul doarme.

Consumul in deep sleep este sub 2 uA, ceea ce il face potrivit pentru un dispozitiv cu baterie mica.

---

## Magistrala I2C

Majoritatea componentelor comunica cu MCU-ul prin I2C pe pinii P0.06 (SDA) si P0.07 (SCL), cu rezistente pull-up de 3.3K. Fiecare componenta are o adresa unica:

| Componenta | Rol | Adresa |
|---|---|---|
| BQ25180 | Charger baterie | 0x6A |
| RT6160 | Regulator 3.3V | 0x75 |
| MAX17048 | Nivel baterie | 0x36 |
| BMA423 | Accelerometru | 0x18 |
| DRV2605 | Motor vibratii | 0x5A |

---

## Display E-Paper

Display-ul de 1.54" (200x200 pixeli) este conectat prin SPI (SCK pe P0.02, MOSI pe P0.03, plus pini de control CS/DC/RST/BUSY). Avantajul e-paper-ului este ca nu consuma energie cand imaginea sta pe loc — consuma doar la refresh.

Alimentarea display-ului este controlata printr-un MOSFET (P1.01) care il opreste complet intre refresh-uri. Se face un refresh partial o data pe minut pentru a actualiza ora, si un full refresh mai rar pentru a elimina ghosting-ul.

---

## Alimentare

Lantul de alimentare functioneaza asa: USB-C (5V) → BQ25180 (incarca bateria si alimenteaza sistemul) → RT6160 (converteste tensiunea bateriei la 3.3V fix) → toate componentele.

BQ25180 are un circuit de power-path, adica sistemul functioneaza si fara baterie daca e conectat la USB. MAX17048 masoara nivelul bateriei si trimite o intrerupere la MCU cand bateria e aproape descarcata.

Pe liniile USB exista o dioda ESD (USBLC6-2SC6Y) care protejeaza circuitul impotriva descarcarilor electrostatice.

---

## Senzori si periferice

**BMA423** — accelerometru cu pedometru hardware integrat. Numara pasii independent, fara sa trezeasca MCU-ul. Trezeste MCU-ul printr-o intrerupere pe P0.08 cand detecteaza miscare sau un anumit numar de pasi.

**DRV2605** — driver pentru motorul de vibratie. MCU-ul ii trimite prin I2C un ID de efect, iar DRV2605 il executa autonom din biblioteca sa de 123 de efecte stocate intern.

**Butoane** — trei butoane (Sus/Jos/Enter) conectate active-low la GND pe pinii P0.13, P0.14 si P1.00. Pot trezi MCU-ul din sleep.

---

## Consum estimat

| Stare | Curent | Timp/zi |
|---|---|---|
| Deep sleep | ~8 uA | ~24h |
| Refresh display (1x/min) | ~8 mA | ~60s total |
| Notificare (BLE + display + vibratii) | ~15 mA | ~100s total |

Total estimat: ~2 mAh/zi → pe o baterie de 250 mAh rezulta o autonomie teoretica de peste 100 de zile. In practica, cu pierderile reale, targetul este de 30 de zile conform specificatiilor proiectului.

# Pini nRF52840 folositi

## I2C — P0.06 (SDA) si P0.07 (SCL)

Acesti doi pini sunt folositi de toate componentele care comunica prin I2C: charger-ul BQ25180,
regulatorul RT6160, fuel gauge-ul MAX17048, accelerometrul BMA423 si driverul haptic DRV2605.
Sunt pini de uz general cu suport hardware I2C si sunt plasati convenabil in schema pentru
rutarea PCB-ului. Pull-up-urile de 3.3K sunt necesare pentru ca I2C are iesiri open-drain.

## SPI — P0.02 (SCK), P0.03 (MOSI), P0.05 (CS)

Folositi pentru comunicatia cu display-ul e-paper. SPI a fost ales in loc de I2C pentru display
deoarece este mult mai rapid, important la refresh-ul imaginii. CS (chip select) pe P0.05
activeaza display-ul doar cand MCU-ul vrea sa ii trimita date.

## Pini de control display — P0.15 (DC), P0.16 (RST), P0.17 (BUSY)

- **DC** (Data/Command): ii spune display-ului daca ce primeste este o comanda sau date de imagine
- **RST** (Reset): reseteaza display-ul la pornire sau dupa o eroare
- **BUSY**: display-ul tine acest pin activ cat timp proceseaza un refresh; MCU-ul asteapta sa
  se elibereze inainte sa trimita date noi

## Power gate display — P1.01

Controleaza MOSFET-ul care opreste alimentarea display-ului cand nu e folosit. Implicit OFF la
reset, activat doar in timpul unui refresh. Economiseste energie intre actualizari.

## Intreruperi

- **P0.08 — BMA423 INT1**: trezeste MCU-ul din deep sleep la detectia de miscare sau pas.
  Folosit ca sursa principala de wake-up pentru activitate fizica.
- **P1.08 — BMA423 INT2**: intrerupere secundara pentru evenimente avansate ale accelerometrului.
- **P0.10 — MAX17048 ALRT**: MCU-ul este notificat cand bateria scade sub un prag configurat,
  pentru a afisa avertismentul de baterie descarcata.
- **P0.11 — BQ25180 /INT**: notifica MCU-ul la evenimente de incarcare (USB conectat/deconectat,
  incarcare completa, eroare).

## Haptic enable — P0.12

Controleaza pinul EN al DRV2605. Cand nu e niciun eveniment haptic, acest pin e LOW si driverul
consuma sub 1 uA. MCU-ul il ridica la HIGH doar inainte sa trimita o comanda de vibratie.

## Butoane — P0.13, P0.14, P1.00

- **P0.13** — buton Sus
- **P0.14** — buton Jos
- **P1.00** — buton Enter / Esc

Toti trei sunt configurati cu pull-up intern si wake-on-low, adica o apasare de buton trezeste
MCU-ul direct din deep sleep fara consum suplimentar.

## USB — USBDP / USBDM (D+ / D-)

Pini dedicati USB ai nRF52840, rutati diferential la conectorul USB-C prin dioda ESD. Folositi
pentru programarea firmware-ului si optional pentru comunicatie cu PC-ul.

## SWD — SWDIO, SWDCLK, nRESET

Pini dedicati de debug si programare, conectati la conectorul TC2030. Folositi cu un programator
J-Link pentru a incarca firmware-ul si pentru debugging in timp real.

# Design Decisions — DRC Approved Errors

DRC-ul a returnat 0 erori si 85 aprobate. Motivele aprobarii:

- **Overlap (35) si Board Outline Clearance (40)**: provin din pozitia butoanelor, care a fost
  stabilita ca cerinta de proiect si nu poate fi modificata.

- **Copper Clearance (9)**: vias-uri care se intersecteaza

- **Copper - Restrict Clearance (1)**: zona restrictionata definita intentionat in jurul antenei
  BLE pentru izolarea ground plane-ului, conform recomandarilor Nordic Semiconductor.


Apache 2.0 — vezi [LICENSE](LICENSE)
