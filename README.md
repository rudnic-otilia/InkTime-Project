# InkTime

Smartwatch open-source bazat pe nRF52840, cu display e-paper.

## Diagramă Bloc
[Baterie LiPo] → [Încărcător BQ25180] → [DC/DC RT6160] → [nRF52840]
↓
[Display E-Paper] ←──────────────── SPI ──────────────────── ┤
[IMU BMA423]      ←──────────────── I2C ──────────────────── ┤
[Flash W25Q512]   ←──────────────── SPI ──────────────────── ┤
[Vibrator]        ←──────────────── GPIO ─────────────────── ┤
[Butoane x3]      ──────────────── GPIO ──────────────────── ┘

## BOM (Bill of Materials)

# Bill of Materials — InkTime

## Componente principale

| Referință | Componentă | Descriere | Package | Cantitate | JLCPCB / LCSC | Datasheet |
|-----------|-----------|-----------|---------|-----------|---------------|-----------|
| U1 | NRF52840-QIAA-R | MCU principal + BLE 5.0 + USB nativ | aQFN-73 (7×7mm) | 1 | [C190794](https://jlcpcb.com/partdetail/NordicSemicon-NRF52840_QIAAR/C190794) | [Datasheet](https://infocenter.nordicsemi.com/pdf/nRF52840_PS_v1.7.pdf) |
| IC1 | BQ25180YBGR | Charger LiPo cu power-path, I2C | DSBGA-8 (1.6×1.1mm) | 1 | [C3682423](https://jlcpcb.com/partdetail/TexasInstruments-BQ25180YBGR/C3682423) | [Datasheet](https://www.ti.com/lit/ds/symlink/bq25180.pdf) |
| IC9 | RT6160AWSC | Buck-boost regulator 3.3V, I2C | WLCSP-15 (1.4×2.3mm) | 1 | [C7065276](https://jlcpcb.com/partdetail/RichTek-RT6160AWSC/C7065276) | [Datasheet](https://www.richtek.com/assets/product_file/RT6160A/DS6160A-00.pdf) |
| U3 | MAX17048G+T10 | Fuel gauge baterie LiPo, I2C | DFN-8 (2×2mm) | 1 | [C2682616](https://jlcpcb.com/partdetail/MaximIntegrated-MAX17048GT10/C2682616) | [Datasheet](https://www.analog.com/media/en/technical-documentation/data-sheets/MAX17048-MAX17049.pdf) |
| IC3 | BMA423 | Accelerometru 3-axe + pedometru, I2C | LGA-12 (2×2mm) | 1 | [C5242966](https://jlcpcb.com/partdetail/Bosch-BMA423/C5242966) | [Datasheet](https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bma423-ds000.pdf) |
| IC2 | DRV2605YZFR | Haptic driver pentru motor ERM, I2C | DSBGA-9 (1.44×1.44mm) | 1 | [C527464](https://jlcpcb.com/partdetail/TexasInstruments-DRV2605YZFR/C527464) | [Datasheet](https://www.ti.com/lit/ds/symlink/drv2605.pdf) |
| D3 | USBLC6-2SC6Y | Protecție ESD linii USB D+/D- | SOT-23-6 | 1 | [C2827693](https://jlcpcb.com/partdetail/STMicroelectronics-USBLC62SC6Y/C2827693) | [Datasheet](https://www.st.com/resource/en/datasheet/usblc6-2.pdf) |
| Q3 | SI1308EDL-T1-GE3 | N-channel MOSFET, power gate e-paper | SC-70-3 | 1 | [C10487](https://jlcpcb.com/partdetail/VishayIntertech-SI1308EDLT1GE3/C10487) | [Datasheet](https://www.vishay.com/docs/63587/si1308edl.pdf) |
| Q1 | DMG2305UX-7 | P-channel MOSFET, power switch | SOT-23-3 | 1 | [C252544](https://jlcpcb.com/partdetail/Diodes-DMG2305UXT116/C252544) | [Datasheet](https://www.diodes.com/assets/Datasheets/DMG2305UX.pdf) |
| J4 | KH-TYPE-C-16P | Conector USB-C 16 pini | SMD | 1 | [C2765186](https://jlcpcb.com/partdetail/Kinghelm-KH_TYPEC_16P/C2765186) | [Datasheet](https://www.kinghelm.net/usb-connectors/kh-type-c-16p.html) |
| J1 | 503480-2400 | Conector FPC 0.5mm 24 pini, pentru display e-paper | SMD | 1 | [C262280](https://jlcpcb.com/partdetail/Molex-5034802400/C262280) | [Datasheet](https://www.molex.com/en-us/products/part-detail/503480-2400) |
| J2 | TC2030-IDC | Conector Tag-Connect SWD debug/programare | PCB footprint | 1 | — (hand assembly) | [Datasheet](https://www.tag-connect.com/wp-content/uploads/bsk-pdf-manager/TC2030-IDC_1.pdf) |
| ANT1 | 2450AT18B100E | Antenă chip 2.4GHz pentru BLE | SMD | 1 | [C89771](https://jlcpcb.com/partdetail/Johanson-2450AT18B100E/C89771) | [Datasheet](https://www.johansontechnology.com/datasheets/2450AT18B100E/2450AT18B100E.pdf) |
| X1 | Cristal 32MHz | Crystal HFXO pentru nRF52840 | SMD 2016 | 1 | [C9002](https://jlcpcb.com/partdetail/C9002) | — |
| X2 | Cristal 32.768kHz | Crystal LFXO pentru RTC | SMD 3215 | 1 | [C32346](https://jlcpcb.com/partdetail/C32346) | — |
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

## Note

- Pasivele 0201 sunt standard și pot fi comandate de la orice furnizor LCSC/JLCPCB.
- Componentele marcate **hand assembly** (J2 TC2030, display FPC, baterie, motor) trebuie asamblate manual.
- Display-ul e-paper (1.54", 200×200px) și bateria LiPo (250mAh) se bugetează separat — nu sunt în BOM-ul PCB.

## Funcționalitate Hardware

**Microcontroller:** nRF52840 — procesor ARM Cortex-M4, Bluetooth 5.0, 1MB Flash, 256KB RAM.

**Alimentare:** Baterie LiPo încărcată prin USB-C via BQ25180. Tensiunea este reglată la 3.3V prin DC/DC RT6160.

**Display:** E-paper conectat prin SPI la nRF52840. Consum foarte mic în standby.

**IMU:** BMA423 conectat prin I2C — accelerometru pentru detectarea mișcării și numărarea pașilor.

**Memorie externă:** W25Q512 prin SPI pentru stocare date.

**Interfețe de comunicație:**
- SPI: Display, Flash
- I2C: IMU
- USB: Încărcare + programare
- SWD: Debug/programare firmware

## Pini nRF52840 utilizați

| Pin | Semnal | Componentă |
|---|---|---|
| P0.13 | EPD_CS | Display |
| P0.14 | EPD_DC | Display |
| P0.15 | EPD_RST | Display |
| P0.16 | EPD_BUSY | Display |
| P0.20 | SWDIO | Debug |
| P0.18 | SWDCLK | Debug |
| P0.26 | SDA | IMU |
| P0.27 | SCL | IMU |

## Decizii de Design

- Grosime PCB: 1mm (conform specificațiilor)
- Rutare pe 4 layere
- Condensatoare de decuplare 100nF plasate lângă fiecare pin de alimentare
- Antena nRF52840 orientată spre exteriorul PCB-ului, cu decupaj sub ea


Apache 2.0 — vezi [LICENSE](LICENSE)
