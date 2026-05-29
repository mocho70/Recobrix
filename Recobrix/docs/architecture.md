# 🏛️ Arquitectura del Sistema - Recobrix

Este documento detalla el diseño arquitectónico de **Recobrix**, un software de tipo SaaS (Software as a Service) enfocado en la eficiencia operativa para la recuperación de cartera de salud.

---

## 🎯 Filosofía del Diseño
El sistema está construido bajo principios de software limpio, buscando separar estrictamente la lógica de presentación (Frontend) de la lógica de negocio y las conexiones a bases de datos (Backend en PHP).

---

## 🌐 Diagrama de Contexto (Modelo C4)

El siguiente esquema describe los límites del sistema y cómo interactúan los actores con la plataforma:

```text
+-------------------+              +-------------------------+
|  Gestor / Cliente | -----------> |        RECOBRIX         |
| (Usuario Empresa) |  Usa el SaaS |   (Plataforma Web)      |
+-------------------+              +-------------------------+
                                                |
                                                | Consulta / Consulta de estados
                                                v
                                   +-------------------------+
                                   |   Entidades de Salud    |
                                   |   (EPS / ARL / AFP)     |
                                   +-------------------------+