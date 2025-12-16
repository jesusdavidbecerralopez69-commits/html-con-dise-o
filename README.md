# Proyecto de Diseño Web Adaptativo con Media Queries

Este repositorio contiene la solución a una serie de ejercicios prácticos sobre **Responsive Web Design** (RWD) utilizando Media Queries.

## 📝 Estrategia Global: Mobile First

Mi elección fue implementar la estrategia **Mobile First** para el diseño global del proyecto (ejercicios 1, 2, 5, 6, 7, 8, 10, 11 y 12).

### 💡 Justificación de la Elección:

1.  **Priorización de Contenido y Rendimiento:** Al empezar con el diseño más pequeño, nos enfocamos en el contenido esencial. Esto resulta en una hoja de estilos base más ligera, lo cual es fundamental para la velocidad de carga en redes móviles y dispositivos menos potentes.
2.  **Sencillez en la Sobrescritura:** Es más fácil añadir estilos y expandir la complejidad (usando `min-width`) que deshacer y anular estilos complejos de escritorio (usando `max-width`). La cascada de CSS trabaja a nuestro favor.
3.  **Filosofía de Progresión:** La estrategia asegura que todos los usuarios, independientemente de su dispositivo, tengan una experiencia básica y funcional, para luego **mejorarla progresivamente** en pantallas más grandes.

---

## 📐 Breakpoints Utilizados y su Lógica

Se definieron tres breakpoints principales para manejar los cambios de diseño:

| Breakpoint | Valor | Dispositivos Destino | Cambios Implementados (Ejemplos) |
| :--- | :--- | :--- | :--- |
| **Base (Mobile)** | 0px - 767px | Teléfonos Inteligentes | Menú apilado (columna), Galería de 1 columna, Tarjetas apiladas. |
| **Tablet** | `@media (min-width: 768px)` | Tabletas, Laptops Pequeñas | Cambio de color de fondo a Azul, Menú alineado, Galería a 2 columnas, Formulario a 2 columnas. |
| **Escritorio Medio** | `@media (min-width: 992px)` | Monitores Estándar | Cambio de color de fondo a Naranja, Galería a 3 columnas, Aumento de tamaño de fuente. |
| **Escritorio Grande** | `@media (min-width: 1200px)` | Monitores Grandes | Galería a 4 columnas, Ajuste de la fuente base (`html`) usando **REM** para un escalado uniforme. |

---

## 🧩 Implementación de Estrategias Específicas

Se implementaron proyectos separados para contrastar ambos enfoques, tal como se solicitó:

* **Mobile First (Ejercicio 3):**
    * **Archivo:** `mobile-first.css`
    * **Lógica:** Los elementos tienen un fondo **verde** por defecto (móvil, ancho completo) y cambian a **azul** con ancho parcial (`45%`) a partir de `768px`.
* **Desktop First (Ejercicio 4):**
    * **Archivo:** `desktop-first.css`
    * **Lógica:** Los elementos tienen un fondo **rojo** por defecto (escritorio, ancho parcial) y se sobrescriben a **amarillo** con ancho completo (`90%`) usando `max-width: 767px` para el móvil.

---

## 🖨️ Estilos de Impresión (Ejercicio 9)

Se utilizó un Media Query específico `@media print` para optimizar la página para la impresión, asegurando:
* Fondo blanco y texto negro.
* Ocultación de elementos no esenciales como el menú (`header`), pie de página (`footer`) e imágenes de la galería.
* Inclusión de las URLs de los enlaces al lado del texto.

**¡La página está diseñada para adaptarse y ofrecer la mejor experiencia tanto en pantalla como en papel!**