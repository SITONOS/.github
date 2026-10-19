# SITONOS Agro-Industrial Technologies

<div align="center">

[![Status](https://img.shields.io/badge/Status-Active%20Development-00E676?style=for-the-badge&logo=statuspage&logoColor=white)](#)
[![Fintech](https://img.shields.io/badge/Fintech-Open%20Banking%20Bancaribe-1976D2?style=for-the-badge&logo=bank&logoColor=white)](#)
[![Dark Theme](https://img.shields.io/badge/Theme-Dark%20Enforced-0A0F1D?style=for-the-badge&logo=shadow&logoColor=white)](#)
[![Clean Code](https://img.shields.io/badge/Architecture-Clean%20Code%20SAST-FF5252?style=for-the-badge&logo=security&logoColor=white)](#)

### 🌾 Conectando el Campo con la Finanza Digital y la Logística Inteligente
*Ganadores del 1.er Lugar — Shark Bank Bancaribe*

---
</div>

## 🏢 Sobre SITONOS

**SITONOS** es un ecosistema tecnológico integral diseñado para modernizar y dinamizar el sector agroindustrial en Venezuela y Latinoamérica. Unificamos la comercialización de cosechas a través de contratos digitales protegidos por custodia de fondos (*Escrow*), telemetría satelital GPS para transporte de carga a granel y liquidación bancaria automatizada.

---

## 🏗️ Arquitectura del Ecosistema

```mermaid
flowchart TD
    Core["🌾 SITONOS ECOSYSTEM CORE"]
    
    subgraph Clients["📱 Canales & Clientes"]
        App["📱 sitonos-app<br/><b>Android Nativo (Kotlin)</b><br/>Productores & Agroindustria"]
        Transport["🚚 sitonos-transport<br/><b>Android & Telemetría GPS</b><br/>Logística & Pesaje Romana"]
        Web["💻 sitonos-web<br/><b>Next.js 16 + React 19</b><br/>Backoffice & Conciliación"]
    end

    subgraph Backend["☁️ Infraestructura & Open Banking"]
        FB["🔥 Firebase Cloud Platform<br/>Firestore RBAC • Auth • Storage"]
        Bank["🏛️ Bancaribe Open Banking (WSO2)<br/>Custodia Escrow • Webhooks • B2P/C2P"]
    end

    Core --> App
    Core --> Transport
    Core --> Web
    App --> FB
    Transport --> FB
    Web --> FB
    FB <--> Bank
```

---

## 📦 Repositorios Principales

| Repositorio | Descripción | Stack Tecnológico |
| :--- | :--- | :--- |
| **`sitonos-app`** | App Android móvil para productores y compradores de cosechas | Kotlin, Jetpack Compose / XML, Coroutines, Dark Theme |
| **`sitonos-transport`** | Módulo de telemetría y transporte para choferes con GPS y QR | Kotlin, Google Maps Platform, Sensor Telemetry |
| **`sitonos-web`** | Portal web de administración, analítica y conciliación financiera | Next.js 16, React 19, Tailwind CSS, Leaflet |
| **`sitonos-docs`** | Especificaciones de APIs Open Banking (WSO2), arquitectura y seguridad | Markdown, Open Banking Specs |

---

## 🔒 Estándares de Ingeniería & Seguridad

- **Auditoría Continua SAST & OWASP:** Componentes no exportados, cero claves expuestas en código fuente y validación estricta de intents y tokens.
- **Dark Theme Enforced:** Interfaz con diseño visual consistente en `#0A0F1D` / `#121212`.
- **Clean Architecture & SRP:** Separación modular estricta entre vista, lógica de negocio y consumo de APIs bancarias.

---

<div align="center">
  <sub>© SITONOS Agro-Industrial Technologies. Todos los derechos reservados.</sub>
</div>
