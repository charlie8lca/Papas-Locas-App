# 🍟 Papas Lab — App de Pedidos a Domicilio

App web móvil para pedidos a domicilio de Papas Lab. Un solo archivo HTML, sin dependencias, lista para publicar.

## ✨ Funcionalidades

- Menú completo con categorías y productos agotados
- Personalización: tamaño (chica / mediana / grande) y toppings
- Oferta del día con descuento automático
- Validación de zona de cobertura
- Carrito persistente (localStorage)
- Checkout con validación de campos obligatorios
- Confirmación de pedido por WhatsApp con mensaje pre-armado
- Soporte para modo oscuro

## 🚀 Publicación rápida

1. Descarga `index.html`
2. Edita el número de WhatsApp (ver configuración abajo)
3. Arrastra el archivo a [netlify.com/drop](https://netlify.com/drop)

## ⚙️ Configuración

Abre `index.html` y busca el bloque `CONFIGURACIÓN` al inicio del `<script>`:

```js
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
// CONFIGURACIÓN — edita aquí tu número
// ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
const WSP_NUM = '521XXXXXXXXXX'; // <-- pon tu número con código de país sin +

// Oferta del día — cambia esto cada día sin tocar nada más
const OFERTA_CONFIG = {
  titulo: 'Oferta del día',
  descripcion: 'Papas Especiales con 20% de descuento',
  producto: 'Papas Especiales',
  descuento: 0.20,
  tag: 'HOY'
};
```

**Número de WhatsApp:** incluye el código de país sin `+`. Ejemplo para México: `5214421234567`

**Oferta del día:** cambia `descripcion`, `producto` y `descuento` cada día. No necesitas tocar nada más del código.

## 🗺️ Zonas de cobertura

Las colonias disponibles se editan en el `<select id="f-colonia">` dentro del HTML:

```html
<option value="Centro">Centro Histórico</option>
<option value="Cumbres">Cumbres</option>
<option value="Juriquilla">Juriquilla</option>
<option value="El Pueblito">El Pueblito</option>
<option value="Constituyentes">Constituyentes</option>
```

Agrega o elimina `<option>` según tu zona real.

## 📁 Estructura del proyecto

```
papas-lab/
└── index.html   ← toda la app en un solo archivo
```

## 🛠️ Tecnologías

- HTML5 / CSS3 / JavaScript vanilla
- [Tabler Icons](https://tabler.io/icons)
- [Google Fonts](https://fonts.google.com) — Fredoka + DM Sans
- localStorage para persistencia del carrito

## 📱 Instalar como app (PWA)

Una vez publicada, los usuarios pueden tocar **"Agregar a pantalla de inicio"** desde Chrome o Safari para instalarla como app nativa sin pasar por la App Store.

---

*Papas Lab App — 2025*
