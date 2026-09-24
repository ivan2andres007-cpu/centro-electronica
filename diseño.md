# Guía de Diseño y Estilo Visual Apple Pro / Modern Dark - Punto Prisma

Esta especificación detalla las reglas de diseño tipográfico, jerarquía visual, paleta de colores y componentes para Punto Prisma, inspiradas en los estándares de Apple Human Interface Guidelines (HIG) y paneles de control modernos (tipo DiBold).

---

## 1. Filosofía y Estética General

- **Sensación Premium y Minimalista**: Limpieza visual absoluta, enfoque en el contenido, eliminación de saturación innecesaria.
- **Modo Oscuro Profundo (Apple Dark Canvas)**:
  - Fondo primario: `#0a0f1d` / `#0f172a` (Slate profundo con matiz azul noche).
  - Superficies de tarjetas y paneles (`card-apple`): `rgba(22, 32, 58, 0.72)` a `rgba(30, 41, 59, 0.8)` con `backdrop-filter: blur(20px)`.
  - Bordes tenues: `1px solid rgba(255, 255, 255, 0.08)`.
  - Sombras: sombras suaves y difusas multicapa (`box-shadow: 0 10px 30px -5px rgba(0, 0, 0, 0.5)`).

---

## 2. Tipografía y Jerarquía

- **Fuente Principal**: `'Inter', -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'Segoe UI', sans-serif`.
- **Figuras Tabulares (`tnum`)**:
  - Todos los números financieros, stocks y cantidades deben utilizar `font-variant-numeric: tabular-nums` para alineación perfecta de columnas.
- **Escala Tipográfica**:
  - Títulos principales de sección: `text-2xl font-bold tracking-tight text-white`.
  - Subtítulos y descripciones: `text-xs font-medium text-slate-400`.
  - Etiquetas y metadatos: `text-[11px] font-semibold uppercase tracking-wider text-slate-400`.
  - Importes destacados: `text-2xl font-black text-emerald-400 tracking-tight font-mono`.

---

## 3. Paleta Cromática y Acentos Semánticos

- **Acento Primario (Teal / Cyan Apple)**: `#06b6d4` a `#0ea5e9` (resaltado, acciones principales, selección activa).
- **Éxito / Ingresos (Emerald Apple)**: `#10b981` / `#34d399` (ventas, cajas abiertas, stocks óptimos).
- **Advertencia / Transición (Amber / Orange)**: `#f59e0b` / `#fb923c` (stocks mínimos, remitos en tránsito).
- **Peligro / Salidas (Rose / Crimson)**: `#f43f5e` / `#ef4444` (gastos, pérdidas, bloqueos, cajas cerradas).
- **Moneda Oficial**: Siempre prefijada con `Gs.` y separador de miles con punto (`Gs. 1.250.000`), sin decimales.

---

## 4. Componentes de UI

### A. Botones Apple
- Bordes redondeados sutiles (`rounded-xl` o `rounded-full`).
- Transición suave al presionar: `active:scale-[0.97] transition-all duration-150`.
- Gradientes sutiles y resplandores en estados activos.
- Estado deshabilitado: `opacity-40 cursor-not-allowed transform-none filter grayscale-[30%]`.

### B. Tablas Estilo Apple
- Encabezados fijos adhesivos con desenfoque (`sticky top-0 bg-slate-900/80 backdrop-blur-md`).
- Separadores delgados `border-slate-800/60`.
- Filas con efecto sutil en hover (`hover:bg-white/[0.04] transition-colors`).
- Badges semánticos en formato píldora (`px-2.5 py-0.5 rounded-full text-xs font-semibold`).

### C. Modales Flotantes
- Fondo translúcido inmersivo: `bg-slate-950/75 backdrop-blur-xl`.
- Tarjeta central con animación de escala sutil (`scale-95 to scale-100`).
- Encabezado con título limpio y botón de cierre discreto con efecto circular en hover.