# Upnify: List Clients

Retrieves clients from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-clients?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-clients?${params}`, {
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
| `periodo` | number | no | Permite filtrar los registros por fecha de creación. - 1 Hoy. - 2 Ayer. - 3 Esta semana. - 4 Semana anterior. - 5 Este mes. - 6 Mes anterior. - 8 Este año. - 10 Año anterior. - 17 Trimestre actual. - 18 Trimestre anterior. |
| `fechaInicio` | date | no | Permite filtrar los registros a partir de esta fecha. |
| `fechaFin` | date | no | Permite filtrar los registros hasta esta fecha. |
| `periodoUltimoContacto` | number | no | Permite filtrar los registros por fecha de último seguimiento. - 1 Hoy. - 2 Ayer. - 3 Esta semana. - 4 Semana anterior. - 5 Este mes. - 6 Mes anterior. - 8 Este año. - 10 Año anterior. - 17 Trimestre actual. - 18 Trimestre anterior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anticipos": 1,
      "apellidos": "string",
      "aprobacionEstado": 1,
      "archivado": 1,
      "calle": "string",
      "canalizado": "string",
      "canalizo": "string",
      "ciudad": "string",
      "codigoPostal": "string",
      "colonia": "string",
      "comentarios": "string",
      "compartido": 1,
      "compartidoCon": {},
      "compartidoConmigo": 1,
      "contacto": "string",
      "corporativo": "string",
      "correo": "string",
      "correoValidado": 1,
      "correoValido": 1,
      "cp1": "string",
      "cp100": "string",
      "cp1e": "string",
      "cp60e": "string",
      "descartado": 1,
      "descartadoFecha": "2026-05-07T12:00:00.000Z",
      "descartadoRazon": "string",
      "diasSinComprar": 1,
      "ejecutivoCorreo": "string",
      "ejecutivoIniciales": "string",
      "ejecutivoNombre": "string",
      "empresa": "string",
      "empresaEsCliente": true,
      "esCanalizado": 1,
      "esCliente": 1,
      "estado": "string",
      "etiquetas": {},
      "facebook": "string",
      "fase": "string",
      "fechaCanalizado": "2026-05-07T12:00:00.000Z",
      "fechaContacto": "2026-05-07T12:00:00.000Z",
      "fechaPrimerContacto": "2026-05-07T12:00:00.000Z",
      "fechaUltimaModificacion": "2026-05-07T12:00:00.000Z",
      "googlePlus": "string",
      "idEstado": "string",
      "idMunicipio": "string",
      "idPais": "string",
      "indice": 1,
      "industria": "string",
      "linkedIn": "https://example.com",
      "moneda": "string",
      "montoComprado": 1,
      "montoPromedio": 1,
      "movil": "string",
      "movilValido": "string",
      "municipio": "string",
      "nombre": "string",
      "origen": "string",
      "pais": "string",
      "primeraCompra": "2026-05-07T12:00:00.000Z",
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
      "saldo": 1,
      "saldoVencido": 1,
      "sexo": "string",
      "skype": "string",
      "telefono": "string",
      "telefono2": "string",
      "tiempoPrimerRespuesta": "2026-05-07T12:00:00.000Z",
      "tieneArchivos": 1,
      "titulo": "string",
      "tkCliente": "string",
      "tkCorporativo": "string",
      "tkEmpresa": "string",
      "tkFase": "string",
      "tkIndustria": "string",
      "tkOrigen": "string",
      "tkProspecto": "string",
      "tkUsuario": "string",
      "transacciones": 1,
      "twitter": "string",
      "ultimaCompra": "2026-05-07T12:00:00.000Z",
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
| `anticipos` | number | Indica la cantidad monetaria de anticipos realizados por el cliente. |
| `apellidos` | string | Contiene los apellidos del cliente. |
| `aprobacionEstado` | number | Código que indica si el cliente necesita ser aprobado por el dueño de la compañia con la cual se registró el cliente.  - 0 No requiere aprobación.  - 1 Se reuiere aprobación.  - 2 Rechazado. |
| `archivado` | number | Indica si el cliente se encuentra archivado.  - 0 No archivado.  - 1 Archivado. |
| `calle` | string | Contiene el nombre o número de la calle, que forma parte de la ubicación del cliente. |
| `canalizado` | string | Indica el usuario al que se le realizó la canalización. |
| `canalizo` | string | Indica el usuario que realizó la canalización. |
| `ciudad` | string | Contiene el nombre o número de la ciudad, que forma parte de la ubicación del cliente. |
| `codigoPostal` | string | Almacena el codigo postal el cliente. |
| `colonia` | string | Contiene el nombre o número de la colonia, que forma parte de la ubicación del cliente. |
| `comentarios` | string | Contiene un comentario que describe al cliente. |
| `compartido` | number | Indica si el cliente se encuentra actualmente compartido.  - 0 No compartido.  - 1 Compartido. |
| `compartidoCon` | object | Contiene un arreglo de datos que proporciona los datos de ejecutivos con los que está compartido el cliente. |
| `compartidoConmigo` | number | Indica si el cliente se encuentra actualmente compartido con el usuario de la sesion.  - 0 No compartido.  - 1 Compartido. |
| `contacto` | string | Guarda el nombre completo del cliente, uniendo nombre y apellido. |
| `corporativo` | string | En caso de existir, indica el nombre del corporativo al que pertenece la empresa del cliente. |
| `correo` | string | Especifica el correo del cliente. |
| `correoValidado` | number | Indica si el correo del cliente ha sido validado. |
| `correoValido` | number | Indica si el correo del contacto es o no valido.  - 0 Sin validar.  - 1 Correo válido  - 2 Reportado como spam  - 3 No existe |
| `cp1` | string | Contiene el valor del primer campo personalizado para clientes, el cual es establecido por el usuario. |
| `cp100` | string | Contiene el valor del centésimo campo personalizado para clientes, el cual es establecido por el usuario. |
| `cp1e` | string | Contiene el valor del primer campo personalizado para empresas, el cual es establecido por el usuario. |
| `cp60e` | string | Contiene el valor del sexagésimo campo personalizado para empresas, el cual es establecido por el usuario. |
| `descartado` | number | Define si el registro está o no descartado.  - 0 No está descartado.  - 1 Descartado. |
| `descartadoFecha` | date | Fecha en que se descartó el cliente. |
| `descartadoRazon` | string | Razón por la que se descartó al cliente. |
| `diasSinComprar` | number | Especifica el número de días desde la última compra. |
| `ejecutivoCorreo` | string | Correo electrónico del ejecutivo que atendió al cliente. |
| `ejecutivoIniciales` | string | Contiene las iniciales del ejecutivo que atendío al cliente. |
| `ejecutivoNombre` | string | Contiene el nombre del ejecutivo que atendió al cliente. |
| `empresa` | string | Guarda el nombre de la empresa a la que pertenece el cliente. |
| `empresaEsCliente` | boolean | Código que indica si la empresa a la que pertenece el cliente es cliente.  - false No es cliente.  - true Es cliente. |
| `esCanalizado` | number | Almacena un código que define si el registro se encuentra canalizado o compartido.  - 0 Registro no canalizado.  - 1 Registro original o maestro.  - 2 Registro esclavo. |
| `esCliente` | number | Define si el registro es o no cliente.  - 0 No es cliente.  - 1 Es cliente. |
| `estado` | string | Guarda el nombre del estado de un país. |
| `etiquetas` | object | Arreglo de datos que contiene las etiquetas asociadas al cliente. |
| `facebook` | string | Contiene la dirección o nombre de facebook del cliente. |
| `fase` | string | Indica en que fase se encuentra el cliente. |
| `fechaCanalizado` | date | Contiene un formato de fecha que indica cuando el registro fué canalizado. |
| `fechaContacto` | date | Contiene un formato compuesto de fecha y hora, el cual indica la fecha del primer contacto con el cliente. |
| `fechaPrimerContacto` | date | Fecha del primer contacto con el cliente. |
| `fechaUltimaModificacion` | date | Fecha de la última modificación en el registro del cliente. |
| `googlePlus` | string | Contiene la dirección o nombre de google plus del cliente. |
| `idEstado` | string | Contiene el identificador para un estado de un país. |
| `idMunicipio` | string | Contiene el identificador para un municipio de un estado de un país. |
| `idPais` | string | Contiene un código que especifica el país utilizado. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `industria` | string | Indica el nombre o descripción al tipo de industria a la que pertenece la empresa del cliente. |
| `linkedIn` | string | Contiene la dirección o nombre de linkedin del cliente. |
| `moneda` | string | Contiene un código que indica el tipo de moneda elegida para la venta. |
| `montoComprado` | number | Indica la cantidad monetaria total de la suma todas las compras realizadas. |
| `montoPromedio` | number | Indica una cantidad monetaria del monto promedio de las compras realizadas. |
| `movil` | string | Almacena un número de teléfono movil del cliente (Si tiene un valor no númerico, devolvera un String). |
| `movilValido` | string | Código que indica si el móvil registrado ha sido validado.  - 0 No validado.  - 1 Validado. |
| `municipio` | string | Guarda el nombre del municipio del estado de un país. |
| `nombre` | string | Contiene el nombre del cliente. |
| `origen` | string | Guarda el origen desde la cual se originó una oportunidad. |
| `pais` | string | Contiene el nombre del país. |
| `primeraCompra` | date | Contiene la fecha en la que el cliente realizó su primera compra. |
| `propio` | number | Define si el registro pertenece al usuario de la sesion.  - 0 No pertenece.  - 1 Pertenece. |
| `proximoEvento` | string | Contiene un arreglo de datos que proporciona los datos de un evento. |
| `puedeAprobar` | number | Código que indica si el ejecutivo de la sesion tiene permitido ligar el cliente a una empresa.  - 0 No permitido.  - 1 Permitido. |
| `puedeArchivar` | number | Código que indica si el ejecutivo de la sesion tiene permitido archivar el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeCompartir` | number | Código que indica si el ejecutivo de la sesion tiene permitido compartir el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeCrearOportunidad` | number | Código que indica si el ejecutivo de la sesion tiene permitido crearle una oportunidad al cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeDarSeguimiento` | number | Código que indica si el ejecutivo de la sesion tiene permitido dar seguimiento al cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeDescartar` | number | Código que indica si el ejecutivo de la sesion tiene permitido descartar el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeEtiquetar` | number | Código que indica si el ejecutivo de la sesion tiene permitido etiquetar el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeReactivar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reactivar el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeReasignar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reasignar el cliente.  - 0 No permitido.  - 1 Permitido. |
| `puedeRechazar` | number | Código que indica si el ejecutivo de la sesion tiene permitido rechazar la peticion de ligar el cliente a una empresa.  - 0 No permitido.  - 1 Permitido. |
| `puesto` | string | Almacena el puesto que ocupa el cliente en la empresa. |
| `recibirCorreos` | number | Indica si el cliente está dispuesto a recibir correos electrónicos. |
| `saldo` | number | Indica la cantidad monetaria de un saldo. |
| `saldoVencido` | number | Indica la cantidad monetaria de un saldo vencido. |
| `sexo` | string | Guarda el sexo que corresponde al cliente.  - H Hombre.  - M Mujer. |
| `skype` | string | Contiene la dirección o nombre de skype del cliente. |
| `telefono` | string | Almacena el número de teléfono que pertenece al cliente (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | En caso de existir, se guarda un número de teléfono secundario del cliente (Si tiene un valor no númerico, devolvera un String). |
| `tiempoPrimerRespuesta` | date | Tiempo transcurrido desde el primer contacto con el cliente. |
| `tieneArchivos` | number | Código que indica si el cliente tiene archivos asociados.  - 0 No tiene archivos.  - 1 Tiene archivos. |
| `titulo` | string | Almacena el titulo con el que se registra el cliente. |
| `tkCliente` | string | Código token que identifica de forma única a un cliente dentro el sistema. |
| `tkCorporativo` | string | Código token que identifica de forma única a un corporativo dentro el sistema. |
| `tkEmpresa` | string | Código token que identifica de forma única a una empresa dentro el sistema. |
| `tkFase` | string | Código token que corresponde a una fase de cliente. |
| `tkIndustria` | string | Código token que identifica de forma única a una industria dentro el sistema. |
| `tkOrigen` | string | Código token que corresponde a un origen de cliente. |
| `tkProspecto` | string | Código token que identifica de forma única a un cliente dentro el sistema. |
| `tkUsuario` | string | Código token que corresponde a un usuario o ejecutivo del sistema. |
| `transacciones` | number | Especifica el número de transacciones que realizó el cliente. |
| `twitter` | string | Contiene la dirección o nombre de twitter del cliente. |
| `ultimaCompra` | date | Contiene la fecha en la que el cliente realizó su última compra. |
| `ultimoContacto` | string | Contiene una descripción breve que indica el motivo del último cotacto. |
| `ultimoContactoFechaHora` | date | Contiene un formato compuesto por fecha y hora que indica cuando se realizaró el último contacto con el cliente. |
| `ultimoContactoIniciales` | string | Contiene las iniciales del nombre del ejecutivo que realizó el último contacto. |
| `ultimoContactoNombre` | string | Contiene el nombre del ejecutivo que realizó el último contacto. |
| `url` | string | Contiene laq url o dirección del sitio web del cliente. |
| `ventaDirecta` | number | Código que indica si el ejecutivo de la sesion tiene permitido crearle una venta directa al cliente.  - 0 No permitido.  - 1 Permitido. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/clientes` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

