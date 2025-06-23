# Diseño de interfaz gráfica para el control de salidas en Controllino

Este repositorio documenta el desarrollo de la práctica 3: *Diseño de interfaz gráfica para el control de salidas en Controllino*, utilizando el **Controllino Mega** como plataforma de automatización, el entorno **Arduino IDE** para la programación, y una interfaz **HMI STONE** como medio de interacción hombre-máquina.

El objetivo fue crear una interfaz amigable y funcional que permitiera al usuario ajustar dinámicamente el brillo de dos LEDs a través de controles gráficos, y activar/desactivar cada LED mediante botones físicos ubicados en el tablero.

---

## 🛠 Requisitos

- **Controllino Mega** con conexión USB
- **Arduino IDE** configurado con la librería oficial de Controllino  
  👉 [https://www.controllino.com/board-library-setup-in-arduino-ide/](https://www.controllino.com/board-library-setup-in-arduino-ide/)
- Cable USB tipo B
- Cable USB tipo A a A
- Tablero de control con HMI STONE STWC050WT-01
- Software Stone Designer GUI (versión recomendada)
- Módulo TTL a RS232 (ya integrado en el tablero)

---

## 💻 La interfaz HMI STONE

La interfaz fue diseñada utilizando el entorno gráfico **STONE Designer GUI**. El proyecto incluye dos widgets del tipo `SpinBox` que permiten al usuario seleccionar un valor entre 0 y 100, representando el porcentaje del ciclo de trabajo (duty cycle) para el control de brillo de dos LEDs independientes.

### Detalles del diseño:
- **spin_box1**: Controla el duty cycle del primer LED.
- **spin_box2**: Controla el duty cycle del segundo LED.
- Ambos valores se transmiten vía comunicación serial RS232 al Controllino.
- El valor recibido se procesa y se convierte en una señal PWM que modula la intensidad del LED correspondiente.

La interfaz fue cargada al HMI mediante conexión USB directa, siguiendo el procedimiento estándar del fabricante. Se recomienda incluir un widget `label` adicional para visualizar el estado ON/OFF de cada LED en futuras mejoras.

---

## 🔧 Código para Controllino Mega

El código de esta práctica realiza la lectura serial de los valores de los `SpinBox`, los convierte a PWM, y permite encender o apagar cada LED mediante un botón físico. A continuación se detallan las principales funciones:

- **Lectura de interfaz gráfica**: mediante `HMI_get_value()` de la librería personalizada `Procesar_HMI.h`.
- **Conversión PWM**: uso de `map()` para convertir de 0–100 a 0–255.
- **Control de estado**: uso de botones físicos (I16 e I17) para activar/desactivar cada LED de forma independiente.
- **Retroalimentación**: impresión por `Serial` del estado de cada LED y su PWM asociado.

## 📚 Referencias

- [Controllino Mega - Página oficial](https://www.controllino.com/)
- [Guía del tablero de control (PDF del docente)](https://drive.google.com/...)
- [Documentación FSM en C++](https://en.cppreference.com/w/cpp/language/enum)

---

## ✍️ Autores

Erick Ramón - Martin Vinces
Estudiantes de Ingeniería en Telecomunicaciones.
Proyecto realizado para el curso de Contról Digital.

---

## 📄 Licencia

Este proyecto se distribuye con fines educativos. El contenido puede ser reutilizado con la debida atribución.
