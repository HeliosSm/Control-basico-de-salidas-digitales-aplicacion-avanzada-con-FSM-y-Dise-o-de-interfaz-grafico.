# Prácticas de Control Digital: Controllino Mega + HMI

Este repositorio contiene el desarrollo completo de las prácticas 2 y 3 correspondientes al curso de **Control Digital**, realizadas con el controlador industrial **Controllino Mega** y, en la práctica 3, una **interfaz gráfica HMI STONE**.

Cada práctica incluye el código fuente, documentación del diseño, capturas del funcionamiento y un informe técnico en formato IEEE.

---

## 📂 Contenido del repositorio

### 🔧 [Práctica 2 — Control básico de salidas digitales y aplicación avanzada con FSM](./Practica%202/)

Esta práctica se divide en dos partes:
- **Parte A**: Control secuencial de una matriz 3x3 de LEDs mediante tres botones físicos (modo espiral normal, inverso y reinicio).
- **Parte B**: Simulación de un sistema de semáforos con lógica de Máquina de Estados Finita (FSM) no bloqueante.

📁 Código y evidencia → [Ir a la carpeta Practica 2](./Practica%202/)

---

### 🖥️ [Práctica 3 — Diseño de interfaz gráfica para el control de salidas](./Practica%203/)

Esta práctica integra una **interfaz HMI STONE** conectada al Controllino Mega. A través de dos `spin_box`, el usuario puede modificar el duty cycle (PWM) de dos LEDs. El encendido y apagado de cada LED se realiza mediante botones físicos. Toda la lógica de interacción está gestionada en el microcontrolador.

📁 Código, interfaz y documentación → [Ir a la carpeta Practica 3](./Practica%203/)

---

## 📚 Información adicional

- Ambas prácticas fueron desarrolladas en **Arduino IDE**.
- El hardware está basado en el **Controllino Mega** y tablero de control académico.
- Se utilizan conceptos como: FSM, PWM, temporización no bloqueante (`millis()`), estructuras (`enum`, `struct`), y comunicación serial con HMI.

---

## ✍ Autores

**Erick Ramón** — **Martin Vinces**  
Estudiantes de Ingeniería en Telecomunicaciones  
Proyecto académico para el curso de *Control Digital* — 2025

---

## 📄 Licencia

Este repositorio se distribuye con fines educativos.  
El contenido puede ser reutilizado citando a los autores.
