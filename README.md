# Proyecto_DeliveryBot_SARASANDOVAL
PROYECTO 
DeliveryBot - Sistema de Pedidos para Cafetería
 
Descripción
 
DeliveryBot es una solución de automatización desarrollada en n8n que utiliza Telegram como interfaz para la gestión de pedidos de cafetería en entornos institucionales. Su objetivo es reducir tiempos de espera, evitar errores en la toma de pedidos y mantener un registro ordenado de ventas y clientes.
 
Tecnologías
 
- Automatización: n8n
- Interfaz de usuario: Telegram Bot
- Almacenamiento: Google Sheets
- Lógica personalizada: JavaScript
 
Estructura de Datos
 
La información se organiza en tres hojas dentro de la hoja de cálculo:
 
1. menu: id_producto, categoria, nombre, precio, stock
2. usuario: telegram_id, nombre, departamento, fecha_registro
3. pedidos: id_pedido, telegram_id, detalle, total, estado, fecha
 
Acceso completo a la hoja de cálculo:
https://docs.google.com/spreadsheets/d/15P6O_SdusHUKOE-jeV1VJ50r_nFn3nIM8VDpdGAa8-g/edit?usp=sharing
 
Funcionamiento
 
1. El usuario inicia la conversación en Telegram
2. Se presenta el menú por categorías
3. Se seleccionan productos y se agrega al pedido
4. Se solicitan datos del cliente
5. Se confirma el pedido y se registra automáticamente
6. El pedido queda con estado PENDIENTE para su preparación
 
Configuración
 
Requisitos previos:
 
- Instalación de n8n activa
- Token de bot de Telegram
- Acceso autorizado a Google Sheets
 
Orden del flujo de trabajo en n8n:
Telegram Trigger → Consulta de menú → Lógica de selección → Envío de mensajes → Registro de datos → Almacenamiento en hojas
