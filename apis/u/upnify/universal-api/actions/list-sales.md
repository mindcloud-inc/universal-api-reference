# Upnify: List Sales

Retrieves sales from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sales
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sales?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sales?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aprobacionEstado` | number | no | Indica el status de asignacion de contacto a compania. - 0 Aprobado. - 1 Pendiente. - 2 Rechazado. Default: `0`. |
| `canalizado` | number | no | Indica si el contacto ha sido canalizado. - 0 No canalizado. - 1 Canalizado. |
| `compartido` | number | no | Indica si el contacto ha sido compartido. - 0 No compartido. - 1 Compartido. |
| `tkUsuario` | string | no | Permite filtrar los registros por un usuario en particular. |
| `tkGrupo` | string | no | Permite filtrar los registros por un grupo en particular. |
| `tkIndustria` | string | no | Permite filtrar los registros por una industria en particular. |
| `tkEtiqueta` | string | no | Permite filtrar los registros por una etiqueta en particular. |
| `tkFase` | string | no | Permite filtrar los registros por una fase en particular. |
| `tkOrigen` | string | no | Permite filtrar los registros por un origen en particular. |
| `tkCorporativo` | string | no | Permite filtrar los registros por un corporativo en particular. |
| `idPais` | string | no | Permite filtrar los registros por un país en particular. |
| `idEstado` | string | no | Permite filtrar los registros por un estado/región en particular. |
| `sexo` | string | no | Permite filtrar los registros por un genero en particular. - H Hombre. - M Mujer. |
| `puesto` | string | no | Permite filtrar los registros por un puesto en particular. |
| `texto` | string | no | Permite filtrar los registros por un texto en particular. |
| `periodo` | string | no | Permite filtrar los registros por fecha de creación. |
| `periodoUltimoContacto` | string | no | Permite filtrar los registros por fecha de último seguimiento. |
| `tkMoneda` | string | no | Permite filtrar los registros por una moneda en particular. |
| `tkLinea` | string | no | Permite filtrar los registros por una linea en particular. |
| `camposAdicionales` | number | no | Envíe un 1 si dedea que la respuesta devuelva campos personalizados de Prospectos y Oportunidades. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anticiposComision": 1,
      "anticiposMonto": 1,
      "apellidos": "string",
      "aprobacionEstado": 1,
      "archivado": 1,
      "calle": "string",
      "canalizado": "string",
      "canalizo": "string",
      "cantidad": 1,
      "ciudad": "string",
      "codigoPostal": "string",
      "colonia": "string",
      "comentarios": "string",
      "comision": 1,
      "comisionMonto": 1,
      "compartido": 1,
      "compartidoCon": {},
      "compartidoConmigo": 1,
      "concepto": "string",
      "contacto": "string",
      "corporativo": "string",
      "correo": "string",
      "correoValido": 1,
      "cotizacionSimple": {},
      "descartado": 1,
      "descuento": 1,
      "descuentoProductos": 1,
      "ejecutivoIniciales": "string",
      "ejecutivoNombre": "string",
      "empresa": "string",
      "empresaEsCliente": true,
      "esCanalizado": 1,
      "esCliente": 1,
      "estado": "string",
      "etiquetas": {},
      "facebook": "string",
      "facturar": 1,
      "fase": "string",
      "fechaCanalizado": "2026-05-07T12:00:00.000Z",
      "fechaCierreVenta": "2026-05-07T12:00:00.000Z",
      "fechaContacto": "2026-05-07T12:00:00.000Z",
      "fechaProximoPagoVenta": "2026-05-07T12:00:00.000Z",
      "fechaUltimoPagoVenta": "2026-05-07T12:00:00.000Z",
      "folio": "string",
      "ganadaFecha": "2026-05-07T12:00:00.000Z",
      "googlePlus": "string",
      "idEstado": "string",
      "idMunicipio": "string",
      "idPais": "string",
      "impuestos": 1,
      "impuestosCotizacion": {},
      "indice": 1,
      "industria": "string",
      "lineaProducto": "string",
      "linkedIn": "https://example.com",
      "moneda": "string",
      "monto": 1,
      "movil": "string",
      "movilValido": "string",
      "municipio": "string",
      "nombre": "string",
      "origen": "string",
      "pais": "string",
      "porcentajeComision": 1,
      "propio": 1,
      "proximoEvento": "string",
      "puedeAprobar": 1,
      "puedeArchivar": 1,
      "puedeCompartir": 1,
      "puedeCrearOportunidad": 1,
      "puedeDarSeguimiento": 1,
      "puedeDescartar": 1,
      "puedeEtiquetar": 1,
      "puedeReactivar": 1,
      "puedeReasignar": 1,
      "puedeRechazar": 1,
      "puesto": "string",
      "recibirCorreos": 1,
      "referencia": "string",
      "sexo": "string",
      "skype": "string",
      "subtotal": 1,
      "telefono": "string",
      "telefono2": "string",
      "tiempoTranscurrido": 1,
      "tieneArchivos": 1,
      "tieneProductos": 1,
      "tipoDeCambio": 1,
      "titulo": "string",
      "tkCorporativo": "string",
      "tkEmpresa": "string",
      "tkFase": "string",
      "tkIndustria": "string",
      "tkLinea": "string",
      "tkMoneda": "string",
      "tkOportunidad": "string",
      "tkOrigen": "string",
      "tkProspecto": "string",
      "tkUsuario": "string",
      "tkVenta": "string",
      "totalLetras": "string",
      "totalLetrasIngles": "string",
      "twitter": "string",
      "ultimoContacto": "string",
      "ultimoContactoFechaHora": "2026-05-07T12:00:00.000Z",
      "ultimoContactoIniciales": "string",
      "ultimoContactoNombre": "string",
      "url": "https://example.com",
      "ventaDirecta": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anticiposComision` | number | Contiene una cantidad monetaria que representa una comisión. |
| `anticiposMonto` | number | Indica una cantidad monetaria que corresponde a un anticipo. |
| `apellidos` | string | Contiene los apellidos del prospecto al cual se asocia la oportunidad. |
| `aprobacionEstado` | number | Código que indica si el prospecto necesita ser aprobado por el dueño de la compañia con la cual se registró el prospecto.  - 0 No requiere aprobación.  - 1 Se reuiere aprobación.  - 2 Rechazado. |
| `archivado` | number | Indica si la oportunidad se encuentra archivada.  - 0 No archivado.  - 1 Archivado. |
| `calle` | string | Contiene el nombre o número de la calle, que forma parte de la ubicación del prospecto. |
| `canalizado` | string | Indica el usuario al que se le realizó la canalización. |
| `canalizo` | string | Indica el usuario que realizó la canalización. |
| `cantidad` | number | Contiene un monto monetario que indica una cantidad. |
| `ciudad` | string | Contiene el nombre o número de la ciudad, que forma parte de la ubicación del prospecto. |
| `codigoPostal` | string | Almacena el codigo postal el prospecto. |
| `colonia` | string | Contiene el nombre o número de la colonia, que forma parte de la ubicación del prospecto. |
| `comentarios` | string | Contiene un comentario que describe al prospecto. |
| `comision` | number | Almacena una catidad monetaria que corresponde a una comisión. |
| `comisionMonto` | number | Almacena la catidad monetaria que corresponde a una comision. |
| `compartido` | number | Indica si el prospecto se encuentra actualmente compartido.  - 0 No compartido.  - 1 Compartido. |
| `compartidoCon` | object | Contiene un arreglo de datos que proporciona los datos de ejecutivos con los que está compartido el prospecto. |
| `compartidoConmigo` | number | Indica si el prospecto se encuentra actualmente compartido con el usuario de la sesion.  - 0 No compartido.  - 1 Compartido. |
| `concepto` | string | Contiene un título o descripción de concepto para una oportunidad. |
| `contacto` | string | Guarda el nombre completo del prospecto, uniendo nombre y apellido. |
| `corporativo` | string | En caso de existir, indica el nombre del corporativo al que pertenece la empresa del prospecto. |
| `correo` | string | Especifica el correo del prospecto. |
| `correoValido` | number | Indica si el correo del contacto es o no valido.  - 0 Sin validar.  - 1 Correo válido  - 2 Reportado como spam  - 3 No existe |
| `cotizacionSimple` | object | Objeto que almacena la cotizacion simple |
| `descartado` | number | Define si el registro está o no descartado.  - 0 No está descartado.  - 1 Descartado. |
| `descuento` | number | Contiene una cantidad monetaria que indica un descuento. |
| `descuentoProductos` | number | Contiene una cantidad monetaria que indica un descuento aplicado a los productos. |
| `ejecutivoIniciales` | string | Contiene las iniciales del ejecutivo que atendío al prospecto. |
| `ejecutivoNombre` | string | Contiene el nombre del ejecutivo que atendió al prospecto. |
| `empresa` | string | Guarda el nombre de la empresa a la que pertenece el prospecto. |
| `empresaEsCliente` | boolean | Código que indica si la empresa a la que pertenece el cliente es cliente.  - false No es cliente.  - true Es cliente. |
| `esCanalizado` | number | Almacena un código que define si el registro se encuentra canalizado o compartido.  - 0 Registro no canalizado.  - 1 Registro original o maestro.  - 2 Registro esclavo. |
| `esCliente` | number | Define si el registro es o no cliente.  - 0 No es cliente.  - 1 Es cliente. |
| `estado` | string | Guarda el nombre del estado de un país. |
| `etiquetas` | object | Arreglo de datos que contiene las etiquetas asociadas al prospecto. |
| `facebook` | string | Contiene la dirección o nombre de facebook del prospecto. |
| `facturar` | number | Código que indica si la venta ya ha sido facturada. |
| `fase` | string | Indica en que fase se encuentra el prospecto. |
| `fechaCanalizado` | date | Contiene un formato de fecha que indica cuando el registro fué canalizado. |
| `fechaCierreVenta` | date | Contiene un formato compuesto de fecha y hora que indica cuando se finalizó la venta. |
| `fechaContacto` | date | Contiene un formato compuesto de fecha y hora, el cual indica la fecha del primer contacto con el prospecto. |
| `fechaProximoPagoVenta` | date | Contiene un formato compuesto de fecha y hora que indica cuando se realizará el próximo pago de una venta a plazos. |
| `fechaUltimoPagoVenta` | date | Contiene un formato compuesto de fecha y hora que indica cuando se realizó el último pago de una venta a plazos. |
| `folio` | string | Contiene el folio del archivo de cotizacion de la oportunidad en caso de tenerlo. |
| `ganadaFecha` | date | Contiene un formato compuesto de fecha y hora que indica cuando se completó la venta. |
| `googlePlus` | string | Contiene la dirección o nombre de google plus del prospecto. |
| `idEstado` | string | Contiene el identificador para un estado de un país. |
| `idMunicipio` | string | Contiene el identificador para un municipio de un estado de un país. |
| `idPais` | string | Contiene un código que especifica el país utilizado. |
| `impuestos` | number | Contiene un monto monetario que indica la cantidad de impuestos. |
| `impuestosCotizacion` | object | Contiene un arreglo que contiene los objetos de todos los impuesto e impuestos retenidos de la cotizacion. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `industria` | string | Indica el nombre o descripción al tipo de industria a la que pertenece la empresa del prospecto. |
| `lineaProducto` | string | La línea de productos donde surgió la oportunidad de venta. |
| `linkedIn` | string | Contiene la dirección o nombre de linkedin del prospecto. |
| `moneda` | string | Cóntiene un código que define el tipo de moneda utilizada. |
| `monto` | number | Almacena la catidad monetaria que corresponde a un monto. |
| `movil` | string | Almacena un número de teléfono movil del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `movilValido` | string | Código que indica si el móvil registrado ha sido validado.  - 0 No validado.  - 1 Validado. |
| `municipio` | string | Guarda el nombre del municipio del estado de un país. |
| `nombre` | string | Contiene el nombre del prospecto al cual se asocia la oportunidad. |
| `origen` | string | Guarda el origen desde la cual se originó una oportunidad. |
| `pais` | string | Contiene el nombre del país. |
| `porcentajeComision` | number | Contiene un porcentaje que corresponde a la comisión ganada. |
| `propio` | number | Define si el registro pertenece al usuario de la sesion.  - 0 No pertenece.  - 1 Pertenece. |
| `proximoEvento` | string | Contiene un arreglo de datos que proporciona los datos de un evento. |
| `puedeAprobar` | number | Código que indica si el ejecutivo de la sesion tiene permitido ligar el prospecto a una empresa.  - 0 No permitido.  - 1 Permitido. |
| `puedeArchivar` | number | Código que indica si el ejecutivo de la sesion tiene permitido archivar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeCompartir` | number | Código que indica si el ejecutivo de la sesion tiene permitido compartir el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeCrearOportunidad` | number | Código que indica si el ejecutivo de la sesion tiene permitido crearle una oportunidad al prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeDarSeguimiento` | number | Código que indica si el ejecutivo de la sesion tiene permitido dar seguimiento al prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeDescartar` | number | Código que indica si el ejecutivo de la sesion tiene permitido descartar la oportunidad.  - 0 No permitido.  - 1 Permitido. |
| `puedeEtiquetar` | number | Código que indica si el ejecutivo de la sesion tiene permitido etiquetar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeReactivar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reactivar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeReasignar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reasignar la oportunidad.  - 0 No permitido.  - 1 Permitido. |
| `puedeRechazar` | number | Código que indica si el ejecutivo de la sesion tiene permitido rechazar la peticion de ligar el prospecto a una empresa.  - 0 No permitido.  - 1 Permitido. |
| `puesto` | string | Almacena el puesto que ocupa el prospecto en la empresa. |
| `recibirCorreos` | number | Indica si el contacto recibe correos.  - 1 No.  - 2 Si. |
| `referencia` | string | Contiene un comentario referente a la venta. |
| `sexo` | string | Guarda el sexo que corresponde al prospecto.  - H Hombre.  - M Mujer. |
| `skype` | string | Contiene la dirección o nombre de skype del prospecto. |
| `subtotal` | number | Contiene un monto monetario que indica una cantidad subtotal. |
| `telefono` | string | Almacena el número de teléfono que pertenece al prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | En caso de existir, se guarda un número de teléfono secundario del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `tiempoTranscurrido` | number | Cantidad de días desde que se realizó la venta. |
| `tieneArchivos` | number | Código que indica si el prospecto tiene archivos asociados.  - 0 No tiene archivos.  - 1 Tiene archivos. |
| `tieneProductos` | number | Indica si la oportunidad tiene productos registrados.  - 0 Sin productos.  - 1 Con productos. |
| `tipoDeCambio` | number | Indica el valor de la moneda utilizada, con respecto a la moneda nacional. |
| `titulo` | string | Almacena el titulo con el que se registra el prospecto. |
| `tkCorporativo` | string | Identificador unico de un corporativo dentro el sistema. |
| `tkEmpresa` | string | Identificador unico de una empresa dentro el sistema. |
| `tkFase` | string | Identificador unico de una fase de prospecto. |
| `tkIndustria` | string | Identificador unico de una industria dentro el sistema. |
| `tkLinea` | string | Código toeken que corresponde a una línea de productos. |
| `tkMoneda` | string | Identificador unico de una moneda en el sistema utilizada en la oportunidad. |
| `tkOportunidad` | string | Identificador unico de una oportunidad dentro el sistema. |
| `tkOrigen` | string | Identificador unico de un origen de prospecto. |
| `tkProspecto` | string | Identificador unico de un prospecto dentro el sistema. |
| `tkUsuario` | string | Identificador unico de un usuario o ejecutivo del sistema. |
| `tkVenta` | string | Identificador unico de una venta registrada en el sistema. |
| `totalLetras` | string | Contiene la descripción del total de una cotización realizada. |
| `totalLetrasIngles` | string | Contiene la descripción del total en inglés de una cotización realizada. |
| `twitter` | string | Contiene la dirección o nombre de twitter del prospecto. |
| `ultimoContacto` | string | Contiene una descripción breve que indica el motivo del último cotacto. |
| `ultimoContactoFechaHora` | date | Contiene un formato compuesto por fecha y hora que indica cuando se realizaró el último contacto con el prospecto. |
| `ultimoContactoIniciales` | string | Contiene las iniciales del nombre del ejecutivo que realizó el último contacto. |
| `ultimoContactoNombre` | string | Contiene el nombre del ejecutivo que realizó el último contacto. |
| `url` | string | Contiene laq url o dirección del sitio web del prospecto. |
| `ventaDirecta` | number | Código que indica si el ejecutivo de la sesion tiene permitido crearle una venta directa al prospecto.  - 0 No permitido.  - 1 Permitido. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/ventas` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales.md) for the provider-specific parameters and requirements.

