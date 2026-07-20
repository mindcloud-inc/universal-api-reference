# Upnify: Get Prospect

Retrieves a prospect from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-prospect
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-prospect?connectionId=$CONNECTION_ID&tkProspecto=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkProspecto": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-prospect?${params}`, {
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
| `tkProspecto` | string | yes | Código token que identifica a un prospecto de manera única dentro del CRM, del cual se requiere conocer los detalles. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "correoValido": 1,
      "cp1": "string",
      "cp100": "string",
      "cp1e": "string",
      "cp60e": "string",
      "descartado": 1,
      "ejecutivoIniciales": "string",
      "ejecutivoNombre": "string",
      "empresa": "string",
      "empresaEsCliente": 1,
      "esCanalizado": 1,
      "esCliente": 1,
      "estado": "string",
      "etiquetas": {},
      "facebook": "string",
      "fase": "string",
      "fechaCanalizado": "2026-05-07T12:00:00.000Z",
      "fechaContacto": "2026-05-07T12:00:00.000Z",
      "googlePlus": "string",
      "idEstado": "string",
      "idMunicipio": "string",
      "idPais": "string",
      "indice": 1,
      "industria": "string",
      "linkedIn": "https://example.com",
      "movil": "string",
      "movilValido": "string",
      "municipio": "string",
      "nombre": "string",
      "origen": "string",
      "pais": "string",
      "pCatalogo1": "string",
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
      "sexo": "string",
      "skype": "string",
      "telefono": "string",
      "telefono2": "string",
      "tieneArchivos": 1,
      "titulo": "string",
      "tkCorporativo": "string",
      "tkEmpresa": "string",
      "tkFase": "string",
      "tkIndustria": "string",
      "tkOrigen": "string",
      "tkProspecto": "string",
      "tkUsuario": "string",
      "twitter": "string",
      "ultimoContacto": "string",
      "ultimoContactoFechaHora": "2026-05-07T12:00:00.000Z",
      "ultimoContactoIniciales": "string",
      "ultimoContactoNombre": "string",
      "url": "https://example.com",
      "utmDate": "string",
      "utmReferrer": "string",
      "ventaDirecta": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apellidos` | string | Contiene los apellidos del prospecto. |
| `aprobacionEstado` | number | Código que indica si el prospecto necesita ser aprobado por el dueño de la compañia con la cual se registró el prospecto.  - 0 No requiere aprobación.  - 1 Se reuiere aprobación.  - 2 Rechazado. |
| `archivado` | number | Indica si el prospecto se encuentra archivado.  - 0 No archivado.  - 1 Archivado. |
| `calle` | string | Contiene el nombre o número de la calle, que forma parte de la ubicación del prospecto. |
| `canalizado` | string | Indica el usuario al que se le realizó la canalización. |
| `canalizo` | string | Indica el usuario que realizó la canalización. |
| `ciudad` | string | Contiene el nombre o número de la ciudad, que forma parte de la ubicación del prospecto. |
| `codigoPostal` | string | Almacena el codigo postal el prospecto. |
| `colonia` | string | Contiene el nombre o número de la colonia, que forma parte de la ubicación del prospecto. |
| `comentarios` | string | Contiene un comentario que describe al prospecto. |
| `compartido` | number | Indica si el prospecto se encuentra actualmente compartido.  - 0 No compartido.  - 1 Compartido. |
| `compartidoCon` | object | Contiene un arreglo de datos que proporciona los datos de ejecutivos con los que está compartido el prospecto. |
| `compartidoConmigo` | number | Indica si el prospecto se encuentra actualmente compartido con el usuario de la sesion.  - 0 No compartido.  - 1 Compartido. |
| `contacto` | string | Guarda el nombre completo del prospecto, uniendo nombre y apellido. |
| `corporativo` | string | En caso de existir, indica el nombre del corporativo al que pertenece la empresa del prospecto. |
| `correo` | string | Especifica el correo del prospecto. |
| `correoValido` | number | Indica si el correo del contacto es o no valido.  - 0 Sin validar.  - 1 Correo válido  - 2 Reportado como spam  - 3 No existe |
| `cp1` | string | Contiene el valor del primer campo personalizado para prospectos, el cual es establecido por el usuario. |
| `cp100` | string | Contiene el valor del centésimo campo personalizado para prospectos, el cual es establecido por el usuario. |
| `cp1e` | string | Contiene el valor del primer campo personalizado para empresas, el cual es establecido por el usuario. |
| `cp60e` | string | Contiene el valor del sexagésimo campo personalizado para empresas, el cual es establecido por el usuario. |
| `descartado` | number | Define si el registro está o no descartado.  - 0 No está descartado.  - 1 Descartado. |
| `ejecutivoIniciales` | string | Contiene las iniciales del ejecutivo que atendío al prospecto. |
| `ejecutivoNombre` | string | Contiene el nombre del ejecutivo que atendió al prospecto. |
| `empresa` | string | Guarda el nombre de la empresa a la que pertenece el prospecto. |
| `empresaEsCliente` | number | Código que indica si la empresa a la que pertenece el prospecto es cliente.  - false No es cliente.  - true Es cliente. |
| `esCanalizado` | number | Almacena un código que define si el registro se encuentra canalizado o compartido.  - 0 Registro no canalizado.  - 1 Registro original o maestro.  - 2 Registro esclavo. |
| `esCliente` | number | Define si el registro es o no cliente.  - 0 No es cliente.  - 1 Es cliente. |
| `estado` | string | Guarda el nombre del estado de un país. |
| `etiquetas` | object | Arreglo de datos que contiene las etiquetas asociadas al prospecto. |
| `facebook` | string | Contiene la dirección o nombre de facebook del prospecto. |
| `fase` | string | Indica en que fase se encuentra el prospecto. |
| `fechaCanalizado` | date | Contiene un formato de fecha que indica cuando el registro fué canalizado. |
| `fechaContacto` | date | Contiene un formato compuesto de fecha y hora, el cual indica la fecha del primer contacto con el prospecto. |
| `googlePlus` | string | Contiene la dirección o nombre de google plus del prospecto. |
| `idEstado` | string | Contiene el identificador para un estado de un país. |
| `idMunicipio` | string | Contiene el identificador para un municipio de un estado de un país. |
| `idPais` | string | Contiene un código que especifica el país utilizado. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `industria` | string | Indica el nombre o descripción al tipo de industria a la que pertenece la empresa del prospecto. |
| `linkedIn` | string | Contiene la dirección o nombre de linkedin del prospecto. |
| `movil` | string | Almacena un número de teléfono movil del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `movilValido` | string | Código que indica si el móvil registrado ha sido validado.  - 0 No validado.  - 1 Validado. |
| `municipio` | string | Guarda el nombre del municipio del estado de un país. |
| `nombre` | string | Contiene el nombre del prospecto. |
| `origen` | string | Guarda el origen desde la cual se originó una oportunidad. |
| `pais` | string | Contiene el nombre del país. |
| `pCatalogo1` | string | Primer catálogo personalizado, contiene el id del valor seleccionado de los catálogos adicionales para prospectos, los cuales son elegidos por el usuario. |
| `propio` | number | Define si el registro pertenece al usuario de la sesion.  - 0 No pertenece.  - 1 Pertenece. |
| `proximoEvento` | string | Contiene un arreglo de datos que proporciona los datos de un evento. |
| `puedeAprobar` | number | Código que indica si el ejecutivo de la sesion tiene permitido ligar el prospecto a una empresa.  - 0 No permitido.  - 1 Permitido. |
| `puedeArchivar` | number | Código que indica si el ejecutivo de la sesion tiene permitido archivar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeCompartir` | number | Código que indica si el ejecutivo de la sesion tiene permitido compartir el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeCrearOportunidad` | number | Código que indica si el ejecutivo de la sesion tiene permitido crearle una oportunidad al prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeDarSeguimiento` | number | Código que indica si el ejecutivo de la sesion tiene permitido dar seguimiento al prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeDescartar` | number | Código que indica si el ejecutivo de la sesion tiene permitido descartar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeEtiquetar` | number | Código que indica si el ejecutivo de la sesion tiene permitido etiquetar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeReactivar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reactivar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeReasignar` | number | Código que indica si el ejecutivo de la sesion tiene permitido reasignar el prospecto.  - 0 No permitido.  - 1 Permitido. |
| `puedeRechazar` | number | Código que indica si el ejecutivo de la sesion tiene permitido rechazar la peticion de ligar el prospecto a una empresa.  - 0 No permitido.  - 1 Permitido. |
| `puesto` | string | Almacena el puesto que ocupa el prospecto en la empresa. |
| `recibirCorreos` | number | Indica si el contacto recibe correos.  - 0 No.  - 1 Si. |
| `sexo` | string | Guarda el sexo que corresponde al prospecto.  - H Hombre.  - M Mujer. |
| `skype` | string | Contiene la dirección o nombre de skype del prospecto. |
| `telefono` | string | Almacena el número de teléfono que pertenece al prospecto (Si tiene un valor no númerico, devolvera un String). |
| `telefono2` | string | En caso de existir, se guarda un número de teléfono secundario del prospecto (Si tiene un valor no númerico, devolvera un String). |
| `tieneArchivos` | number | Código que indica si el prospecto tiene archivos asociados.  - 0 No tiene archivos.  - 1 Tiene archivos. |
| `titulo` | string | Almacena el titulo con el que se registra el prospecto. |
| `tkCorporativo` | string | Código token que identifica de forma única a un corporativo dentro el sistema. |
| `tkEmpresa` | string | Código token que identifica de forma única a una empresa dentro el sistema. |
| `tkFase` | string | Código token que corresponde a una fase de prospecto. |
| `tkIndustria` | string | Código token que identifica de forma única a una industria dentro el sistema. |
| `tkOrigen` | string | Código token que corresponde a un origen de prospecto. |
| `tkProspecto` | string | Código token que identifica de forma única a un prospecto dentro el sistema. |
| `tkUsuario` | string | Código token que corresponde a un usuario o ejecutivo del sistema. |
| `twitter` | string | Contiene la dirección o nombre de twitter del prospecto. |
| `ultimoContacto` | string | Contiene una descripción breve que indica el motivo del último cotacto. |
| `ultimoContactoFechaHora` | date | Contiene un formato compuesto por fecha y hora que indica cuando se realizaró el último contacto con el prospecto. |
| `ultimoContactoIniciales` | string | Contiene las iniciales del nombre del ejecutivo que realizó el último contacto. |
| `ultimoContactoNombre` | string | Contiene el nombre del ejecutivo que realizó el último contacto. |
| `url` | string | Contiene laq url o dirección del sitio web del prospecto. |
| `utmDate` | string | Contiene el valor para el rastreo de las campañas, el cual es establecido por el usuario. |
| `utmReferrer` | string | Contiene el valor para el rastreo de las campañas, el cual es establecido por el usuario. |
| `ventaDirecta` | number | Código que indica si el ejecutivo de la sesion tiene permitido crearle una venta directa al prospecto.  - 0 No permitido.  - 1 Permitido. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/prospectos/:tkProspecto` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prospect.md) for the provider-specific parameters and requirements.

