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

| Componentă | Valoare | Capsulă | Cantitate | Link JLC | Datasheet |
|---|---|---|---|---|---|
| nRF52840 | MCU | AQFN50 | 1 | [JLC](https://jlcpcb.com/parts) | [Nordic](https://www.nordicsemi.com) |
| BQ25180 | LiPo Charger | DSBGA-9 | 1 | [JLC](https://jlcpcb.com/parts) | [TI](https://www.ti.com) |
| RT6160 | DC/DC | SOT563 | 1 | [JLC](https://jlcpcb.com/parts) | [Richtek](https://www.richtek.com) |
| BMA423 | IMU | LGA-12 | 1 | [JLC](https://jlcpcb.com/parts) | [Bosch](https://www.bosch-sensortec.com) |
| W25Q512 | Flash 64MB | WSON-8 | 1 | [JLC](https://jlcpcb.com/parts) | [Winbond](https://www.winbond.com) |

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
