# Integrante 4 – Elvis

**Responsabilidad: Analista de historias de usuario. Consolida las historias de usuario y criterios de aceptación con aporte del equipo.**

**Requerimientos asignados: RF-31 a RF-40
Historias asignadas: HU-31 a HU-40**

## RF-31 – Registrar despacho

Requerimiento:
El sistema debe permitir registrar un nuevo despacho.

- **Prioridad:** Alta
Responsable: Integrante 4

### HU-31:
Como Operador logístico, quiero registrar un nuevo despacho, para mantener control sobre las salidas del almacén.

### Criterios de aceptación

- Dado que se completan los datos obligatorios y existe al menos un producto, cuando se confirma, entonces el sistema registra el despacho.

- Dado que el despacho no contiene productos, cuando se intenta confirmar, entonces el sistema no registra la operación.

## RF-32 – Seleccionar destino

Requerimiento:
El sistema debe permitir seleccionar el destino o proyecto correspondiente al despacho.

- **Prioridad:** Alta
Responsable: Integrante 4

### HU-32:
Como Operador logístico, quiero seleccionar el destino o proyecto del despacho, para identificar a dónde se envían los materiales.

### Criterios de aceptación

- Dado que existen destinos registrados, cuando se prepara un despacho, entonces el sistema permite seleccionar uno.

- Dado que no se selecciona un destino requerido, cuando se intenta confirmar, entonces el sistema solicita completar el dato.

## RF-33 – Responsable del despacho

Requerimiento:
El sistema debe permitir registrar al responsable del despacho.

- **Prioridad:** Media
Responsable: Integrante 4

### HU-33:
Como Operador logístico, quiero registrar al responsable del despacho, para identificar quién gestiona la salida.

### Criterios de aceptación

- Dado que se prepara un despacho, cuando se ingresa el responsable, entonces el sistema almacena su nombre.

- Dado que se consulta el despacho, cuando se muestran sus datos, entonces el responsable registrado se visualiza.

## RF-34 – Productos del despacho

Requerimiento:
El sistema debe permitir agregar productos al detalle del despacho.

- **Prioridad:** Alta
Responsable: Integrante 4

### HU-34:
Como Operador logístico, quiero agregar productos al detalle del despacho, para especificar los materiales que serán enviados.

### Criterios de aceptación

- Dado que se selecciona un producto válido, cuando se agrega al despacho, entonces el sistema lo incorpora al detalle.

- Dado que se agregan varios productos, cuando se revisa el detalle, entonces cada producto conserva su cantidad registrada.

## RF-35 – Validar stock

Requerimiento:
El sistema debe validar que exista stock suficiente antes de realizar un despacho.

- **Prioridad:** Alta
Responsable: Integrante 4

### HU-35:
Como Operador logístico, quiero validar el stock antes de despachar, para evitar salidas superiores a las existencias.

### Criterios de aceptación

- Dado que la cantidad solicitada es menor o igual al stock, cuando se valida el despacho, entonces el sistema permite continuar.

- Dado que la cantidad solicitada supera el stock, cuando se valida, entonces el sistema impide confirmar esa salida e informa la insuficiencia.

## RF-36 – Descontar inventario

Requerimiento:
El sistema debe descontar del inventario las cantidades correspondientes a un despacho confirmado.

- **Prioridad:** Alta
Responsable: Integrante 4

### HU-36:
Como Operador logístico, quiero descontar del inventario los productos despachados, para mantener actualizado el stock real.

### Criterios de aceptación

- Dado que un despacho válido es confirmado, cuando se procesa, entonces el sistema descuenta las cantidades despachadas del stock.

- Dado que el despacho se cancela antes de confirmarse, cuando finaliza la operación, entonces el stock no se modifica.

## RF-37 – Consultar despachos

Requerimiento:
El sistema debe permitir consultar los despachos registrados.

- **Prioridad:** Media
Responsable: Integrante 4

### HU-37:
Como Operador logístico, quiero consultar los despachos registrados, para revisar las salidas realizadas.

### Criterios de aceptación

- Dado que existen despachos registrados, cuando se abre la consulta, entonces el sistema muestra el listado de despachos.

- Dado que se selecciona un despacho existente, cuando se consulta, entonces el sistema permite identificar sus datos principales.

## RF-38 – Productos del despacho

Requerimiento:
El sistema debe mostrar los productos incluidos en un despacho.

- **Prioridad:** Media
Responsable: Integrante 4

### HU-38:
Como Operador logístico, quiero visualizar los productos incluidos en un despacho, para verificar qué materiales fueron enviados.

### Criterios de aceptación

- Dado que un despacho contiene productos, cuando se consulta su detalle, entonces el sistema muestra los productos y cantidades.

- Dado que se consulta un despacho válido, cuando se muestra el detalle, entonces los datos corresponden al despacho seleccionado.

## RF-39 – Consultar movimientos

Requerimiento:
El sistema debe permitir consultar los movimientos de entrada y salida de productos.

- **Prioridad:** Media
Responsable: Integrante 4

### HU-39:
Como Administrador u operador autorizado, quiero consultar movimientos de entrada y salida, para dar seguimiento al flujo del inventario.

### Criterios de aceptación

- Dado que existen movimientos registrados, cuando se realiza la consulta, entonces el sistema muestra entradas y salidas almacenadas.

- Dado que se revisa un movimiento, cuando se muestra su información, entonces se identifica el tipo de operación y sus datos asociados.

## RF-40 – Guardar operaciones

Requerimiento:
El sistema debe conservar en la base de datos la información de las operaciones logísticas registradas.

- **Prioridad:** Alta
Responsable: Integrante 4

### HU-40:
Como Administrador, quiero conservar las operaciones logísticas en la base de datos, para mantener un historial persistente del sistema.

### Criterios de aceptación

- Dado que una operación se confirma correctamente, cuando finaliza el proceso, entonces su información queda almacenada en MySQL.

- Dado que el sistema se cierra y vuelve a abrir, cuando se consultan operaciones previamente guardadas, entonces los registros continúan disponibles.