# 🥁 CDC-SAMPLER STUDIO PRO
### *Estación de Muestreo, Síntesis Analógica, Teclado Cromático y Secuenciador Multi-Track en Web Audio DSP*

[![Platform: All Browsers](https://img.shields.io/badge/Platform-Chrome%20%7C%20Edge%20%7C%20Brave%20%7C%20Firefox-orange.svg?style=for-the-badge)](#)
[![Audio Engine: Web Audio API 64-bit](https://img.shields.io/badge/Audio%20Engine-Web%20Audio%2064--bit-blue.svg?style=for-the-badge)](#)
[![Web MIDI: Plug and Play](https://img.shields.io/badge/Web%20MIDI-Plug%20%26%20Play-brightgreen.svg?style=for-the-badge)](#)
[![Transient Slicer: Zero Latency](https://img.shields.io/badge/Transient%20Slicer-Zero%20Latency-green.svg?style=for-the-badge)](#)
[![Design: Skeuomorphic Boutique MPC](https://img.shields.io/badge/UI-Skeuomorphic%20MPC%20Hardware-yellow.svg?style=for-the-badge)](#)
[![Single File: Zero Install](https://img.shields.io/badge/Portability-100%25%20Single%20File%20(HTML)-purple.svg?style=for-the-badge)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-lightgrey.svg?style=for-the-badge)](#)

---

![CDC-SAMPLER STUDIO PRO - Hardware Overview](screenshots/workstation_live.png)

---

## ⚡ Descripción General / Overview

**CDC-SAMPLER STUDIO PRO** es una estación de trabajo de producción musical (*Groovebox / MPC Workstation / Drum Machine*) virtual de alta fidelidad, inspirada en las legendarias máquinas de muestreo hardware (Akai MPC, E-mu SP-1200, Roland TR-808/909). 

Construida con una arquitectura de ingeniería **100% autoportante (Single-File)** sin dependencias externas, compiladores ni dependencias de Node.js, ejecuta un motor de procesamiento de señal digital (**DSP**) de coma flotante de 64 bits directamente en el navegador mediante la **Web Audio API**.

### 🌟 Capacidades Principales
- **Editor OLED de formas de onda** con corte de transitorios y autosegmentación (*Auto-Slicer* en 16 porciones).
- **Doble Modo de Interpretación**:
  - **`16 PADS`**: Matriz de silicona 4x4 con iluminación RGB reactiva, 4 bancos (64 ranuras) y grupos de exclusión (*Choke Groups*).
  - **`CHROMATIC KEYS`**: Teclado de sintetizador de 4 octavas (C2 a C6, 49 teclas) con ancho físico invariable, polifonía real para acordes y transposición por semitonos en tiempo real.
- **Secuenciador Multi-Track (Grid de 16 Pistas)**:
  - Selector de vista: **`1 TRACK`** (edición detallada) vs **`MULTI-TRACK (GRID)`** (16 pistas de instrumentos visibles y editables simultáneamente).
  - Controles individuales de **Mute (`M`)** y **Solo (`S`)** por canal.
  - Reloj lookahead de ultra precisión, swing analógico MPC (50% a 75%), metrónomo y grabación al vuelo.
- **Distribución 50% / 50% con Splitter Interactivo**: Barra divisoria arrastrable con el mouse y reseteo por doble clic.
- **Iconografía Vectorial Profesional (SVG)**: Gráficos vectoriales nítidos de alta gama para transporte, herramientas y selectores.
- **Matriz de Síntesis por Voz**: Envolventes ADSR analógicas, filtro multimodo resonante VCF de 24 dB/oct, y modulación LFO asignable.
- **Rack de Efectos Master Vintage**: Emulador SP-1200 Bitcrusher de 12 bits, Saturador de Cinta cálido, Tape Delay estéreo sincronizado, Reverb algorítmica y Compresor/Limitador de bus.
- **Muestreo en Vivo desde Micrófono/Línea** con medidor de nivel VU estéreo en tiempo real.
- **Control Físico Plug & Play**: Detección nativa de controladores MIDI USB vía **Web MIDI API** y mapeo ergonómico para teclados de computadora.
- **Renderizado Offline a WAV**: Exportación en master estéreo PCM sin pérdida (44.1 kHz, 16 bits), respetando mutes y solos.

---

## 📸 Módulos de Hardware y Capturas de Interfaz

### 1. 🎛️ Pantalla OLED, Forma de Onda y Slicer de Transitorios
Visualización vectorial en tiempo real sobre pantalla OLED reflectiva. Permite arrastrar los marcadores de **Inicio (`START`)** y **Fin (`END`)**, aplicar **Normalización digital de pico**, **Inversión de muestra (`REVERSE`)** y disparar el algoritmo de corte automático **`SLICE TO PADS`** para trocear loops y baterías completas al instante.

![OLED Waveform & Transient Slicer](screenshots/waveform_slicer.png)

### 2. 🎚️ Matriz de Síntesis por Voz & Filtros VCF Analógicos
Cada uno de los 16 pads cuenta con procesamiento de voz independiente:
- **Pestaña ENV / AMP**: Curva de volumen ADSR (Attack, Decay, Sustain, Release), afinación cromática (*Tuning* en semitonos) y panorama estéreo (*Pan*).
- **Pestaña VCF FILTER**: Filtro multimodo (LowPass 24dB, HighPass, BandPass, Notch), frecuencia de corte (*Cutoff*), resonancia (*Q*), profundidad de envolvente (*Env Mod*) y decaimiento (*Env Decay*).
- **Pestaña LFO**: Oscilador de baja frecuencia asignable a Tono, Corte o Panorama con formas de onda senoidal, triangular, cuadrada o sierra.

| Filtro VCF Resonante | Matriz de Efectos Master |
| :---: | :---: |
| ![VCF Filter](screenshots/vcf_filter.png) | ![Master FX](screenshots/master_fx.png) |

### 3. 🎹 Modo Teclado Cromático Polifónico (Voces y Sintetizadores)
Diseñado para interpretar melodías, voces y acordes corales completos utilizando cualquier muestra:
- **4 Octavas Completas (C2 a C6, 49 teclas)**: Teclas blancas fijas a `36px` y negras a `22px` con proporciones físicas naturales invariables (no se deforman al redimensionar la ventana).
- **Polifonía real de voces**: Permite ejecutar acordes simultáneos (tríadas, séptimas, capas vocales) sin cortes abruptos entre voces.
- **Navegación horizontal fluida**: Desplazamiento por rueda de ratón (*scroll wheel*) y auto-centrado suave hacia la octava activa.
- **Selector rápido de Pad**: Menú integrado de mini-pads para cambiar el sonido de la voz melódica con un solo clic.

### 4. 🥁 Secuenciador de Pasos: Vista Single vs Multi-Track (Grid)
- **Modo `1 TRACK`**: Vista clásica para programación detallada con botones de paso grandes para el pad en foco.
- **Modo `MULTI-TRACK (GRID)`**: Matriz estilo drum machine / DAW donde las **16 pistas de instrumentos se visualizan apiladas verticalmente**:
  - Visualización del patrón completo de batería y melodía en una sola pantalla.
  - Botones **`M` (Mute)** y **`S` (Solo)** independientes por pista.
  - Barra de LEDs superior que indica la posición del compás en tiempo real sobre todas las pistas.
  - Resaltado de compases (pasos 1, 5, 9 y 13).

### 5. 🎚️ Splitter Interactivo y Distribución 50% / 50%
Permite adaptar el área de trabajo según la tarea en curso:
- Arrastre con el mouse para expandir el sector de interpretación (Pads / Teclas) o el secuenciador de pasos.
- **Doble clic de restauración**: Restablece instantáneamente la proporción simétrica 50% / 50%.

---

## 📐 Especificaciones de Ingeniería y Arquitectura DSP

```mermaid
graph LR
    subgraph INGESTION ["Entrada de Audio"]
        A1["Micrófono / Entrada de Línea"]
        A2["Importador WAV / MP3 / FLAC"]
        A3["Sintetizadores Analógicos Offline"]
    end

    subgraph VOICE_DSP ["Procesamiento por Voz (x16 Pads / Teclas Polifónicas)"]
        B1["Waveform Slicer / Trimmer"]
        B2["Pitch Shifter / Resampler"]
        B3["ADSR Amp Envelope (Poly Voices)"]
        B4["VCF Multimode Filter (24dB/oct)"]
        B5["LFO Modulation Engine"]
        B6["Choke Logic"]
    end

    subgraph SEQUENCER ["Secuenciador 16 Pistas"]
        S1["Lookahead Clock Engine"]
        S2["Single Track View"]
        S3["Multi-Track Grid View"]
        S4["Mute / Solo Matrix"]
    end

    subgraph MASTER_BUS ["Rack de Efectos Master"]
        C1["SP-1200 12-Bit Crusher"]
        C2["Tape Tube Saturation"]
        C3["Stereo BPM Delay"]
        C4["Algorithmic Reverb"]
        C5["VCA Master Bus Compressor"]
    end

    subgraph OUTPUT ["Salida"]
        D1["AudioContext Destination (Bocinas / Auriculares)"]
        D2["OfflineAudioContext -> WAV Export (16-bit 44.1kHz)"]
    end

    INGESTION --> B1
    B1 --> B2 --> B3 --> B4 --> MASTER_BUS
    B5 -.->|Modula| B2
    B5 -.->|Modula| B4
    B6 -.->|Corta| B3
    SEQUENCER --> VOICE_DSP
    MASTER_BUS --> C1 --> C2 --> C3 --> C4 --> C5
    C5 --> OUTPUT
```

| Especificación | Detalle Técnico |
| :--- | :--- |
| **Pipeline de Procesamiento** | 64-bit Floating-Point DSP Pipeline nativo de `AudioContext` |
| **Latencia de Audio** | `latencyHint: 'interactive'` (~2.8 ms a 5.5 ms con buffers hardware directos) |
| **Reloj de Secuenciación** | Algoritmo Web Audio Lookahead Timer (deriva temporal < 0.5 ms) |
| **Pistas de Secuenciador** | 16 Pistas simultáneas con vista Single y Multi-Track Grid con Mute / Solo |
| **Teclado Cromático** | 4 Octavas (C2-C6, 49 teclas) polifónico con Web MIDI y teclas fijas |
| **Matriz de Pads** | 16 Pads virtuales x 4 bancos (`Bank A`, `Bank B`, `Bank C`, `Bank D`) = 64 sonidos |
| **Slicer Automático** | Detección matemática de transitorios y particionado simétrico 1/16 a pads |
| **Formatos Soportados** | WAV, MP3, AIFF, OGG, FLAC, AAC (decodificación directa vía Web Audio) |
| **Exportación** | Master mixdown estéreo PCM WAV (44.1 kHz, 16 bits) vía `OfflineAudioContext` |
| **Web MIDI** | Integración nativa plug-and-play vía `navigator.requestMIDIAccess` |
| **Iconografía** | Gráficos vectoriales SVG puros con alineación subpixel |
| **Portabilidad** | 100% Single-File HTML / Vanilla JS / CSS3 (Sin node_modules, sin Webpack) |

---

## ⌨️ Mapeo de Teclado de Computadora

### 1. En Modo `16 PADS` (Baterías y Cajas de Ritmo)
```
┌──────────┬──────────┬──────────┬──────────┐
│  [ 1 ]   │  [ 2 ]   │  [ 3 ]   │  [ 4 ]   │
│ RIDE CYM │ COWBELL  │ FM BASS  │ VOCAL CH │  (Pads 13 - 16)
├──────────┼──────────┼──────────┼──────────┤
│  [ Q ]   │  [ W ]   │  [ E ]   │  [ R ]   │
│ LOW TOM  │ MID TOM  │ HIGH TOM │ CRASH CY │  (Pads 09 - 12)
├──────────┼──────────┼──────────┼──────────┤
│  [ A ]   │  [ S ]   │  [ D ]   │  [ F ]   │
│ CLAP     │ CH HAT   │ OPEN HAT │ PEDAL HT │  (Pads 05 - 08)
├──────────┼──────────┼──────────┼──────────┤
│  [ Z ]   │  [ X ]   │  [ C ]   │  [ V ]   │
│ 808 SUB  │ ACOUSTIC │ TRAP SNR │ RIMSHOT  │  (Pads 01 - 04)
└──────────┴──────────┴──────────┴──────────┘
```

### 2. En Modo `CHROMATIC KEYS` (Melodías, Voces y Sintetizadores)
- **Teclas Blancas**: `A` (C), `S` (D), `D` (E), `F` (F), `G` (G), `H` (A), `J` (B), `K` (C+1), `L` (D+1), `Ñ` (E+1), `'` (F+1)
- **Teclas Negras**: `W` (C#), `E` (D#), `T` (F#), `Y` (G#), `U` (A#), `O` (C#+1), `P` (D#+1)
- **Cambio de Octava**: `Z` (bajar octava) / `X` (subir octava)

### 3. Controles Globales de Transporte
- **`Barra Espaciadora`**: Iniciar / Pausar reproducción del secuenciador (`PLAY / PAUSE`).
- **`TAP`**: Ajuste intuitivo de tempo tocando al ritmo deseado con el ratón.
- **`CLICK`**: Conmutación de metrónomo audible para ensayar y grabar en tiempo real.
- **`REC`**: Activación de grabación en vivo sobre los pasos del secuenciador.

---

## 🔌 Embeber en Aplicaciones (.NET / Blazor / Electron / Web)

Al ser una solución de archivo único completamente autónoma y sin dependencias externas, puede integrarse de manera limpia y sin fricción en cualquier stack moderno:

### En Blazor / ASP.NET Core / HTML
```html
<iframe 
    src="index.html" 
    title="CDC Sampler Studio Pro"
    style="width: 100%; height: 95vh; border: none; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.8);"
    allow="microphone; midi">
</iframe>
```

### En .NET MAUI / WPF / WinUI (WebView2)
```csharp
webView.Source = new Uri("file:///path/to/index.html");
```

---

## 🚀 Inicio Rápido / Quick Start

No requiere compilación ni instalación de paquetes (`npm install`).

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/cdcespon/sampler.git
   cd sampler
   ```

2. **Ejecutar:**
   - **Opción A (Doble clic):** Abre directamente [`index.html`](./index.html) en Google Chrome, Microsoft Edge, Brave o Mozilla Firefox.
   - **Opción B (Servidor local ligero para habilitar micrófono y Web MIDI sin restricciones de protocolo `file://`):**
     ```bash
     # Con Python:
     python -m http.server 8080

     # O con Node:
     npx serve .
     ```
   - Abre tu navegador en `http://localhost:8080`.

---

## 🌐 Compatibilidad de Navegadores

| Navegador | Soporte Audio DSP | Web MIDI | Grabación Micrófono | Aceleración Canvas OLED |
| :--- | :---: | :---: | :---: | :---: |
| **Google Chrome** | ✅ 100% | ✅ Nativo | ✅ Si | ✅ 60 FPS |
| **Microsoft Edge** | ✅ 100% | ✅ Nativo | ✅ Si | ✅ 60 FPS |
| **Brave Browser** | ✅ 100% | ✅ Nativo | ✅ Si | ✅ 60 FPS |
| **Mozilla Firefox** | ✅ 100% | ⚠️ Requiere Add-on | ✅ Si | ✅ 60 FPS |
| **Apple Safari** | ✅ 100% | ⚠️ Parcial | ✅ Si | ✅ 60 FPS |

---

## 📄 Licencia

Este proyecto está bajo la Licencia **MIT**. Consulta el archivo de licencia para más detalles.

---

<div align="center">
  <sub>Desarrollado con pasión por el audio digital, los sintetizadores analógicos y la Web moderna. 🎛️⚡</sub>
</div>
