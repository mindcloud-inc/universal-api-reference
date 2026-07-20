# Upnify: List Prospect Opportunities

Retrieves opportunities for a prospect in Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-prospect-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-prospect-opportunities?connectionId=$CONNECTION_ID&tkProspecto=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkProspecto": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-prospect-opportunities?${params}`, {
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
| `tkProspecto` | string | yes | El código token que identifica a un prospecto de manera única dentro del CRM, del cual requerimos consultar las oportunidades asociadas. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivo": "string",
      "cantidad": 1,
      "certeza": 1,
      "cierreEstimado": "2026-05-07T12:00:00.000Z",
      "comision": 1,
      "comisionMonto": 1,
      "concepto": "string",
      "contacto": "string",
      "descartado": 1,
      "ejecutivoNombre": "string",
      "empresa": "string",
      "fase": "string",
      "fechaHora": "2026-05-07T12:00:00.000Z",
      "fechaProximoRecordatorio": "2026-05-07T12:00:00.000Z",
      "fechaUltimoSeguimiento": "2026-05-07T12:00:00.000Z",
      "ganada": "string",
      "ganadaFecha": "2026-05-07T12:00:00.000Z",
      "impuestos": 1,
      "impuestosRetenidos": 1,
      "indice": 1,
      "iniciales": "string",
      "lineaProducto": "string",
      "moneda": "string",
      "monto": 1,
      "montoPagado": 1,
      "perdida": 1,
      "perdidaFecha": "string",
      "perdidaRazon": "string",
      "tieneProductos": 1,
      "tipoDeCambio": 1,
      "tkCerteza": "string",
      "tkFase": "string",
      "tkOportunidad": "string",
      "tkProspecto": "string",
      "tkSeguimiento": "string",
      "tkUsuario": "string",
      "ultimaModificacion": "2026-05-07T12:00:00.000Z",
      "ultimoContactoComentario": "string",
      "ultimoContactoEjecutivo": "string",
      "ultimoContactoFechaHora": "2026-05-07T12:00:00.000Z",
      "ultimoContactoIniciales": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivo` | string | Contiene el nombre con el que el archivo fue almacenado en amazon. Se le añade una cadena adicional aleatoria con el fin de evitar archivos con nombres iguales. |
| `cantidad` | number | Indica el monto monetario que corresonde a la oportunidad. |
| `certeza` | number | Contiene un valor porcentual con base 1, donde 1 es el 100%. |
| `cierreEstimado` | date | Guarda una fecha de cierre para la oportunidad. |
| `comision` | number | Representa una cantidad porcentual en base 1, donde 1 es el 100%. |
| `comisionMonto` | number | Contiene un cantidad monetaria que corresponde a la comisión, tras haber aplicado una comisión porcentual al monto. |
| `concepto` | string | Indica el concepto de la oportunidad aociada al prospecto. |
| `contacto` | string | Contiene el comentario del último seguimiento realizado. |
| `descartado` | number | Código que indica si la oportunidad se encuentra descartada.  - 0 Oportunidad no descartada.  - 1 Oportunidad descartada. |
| `ejecutivoNombre` | string | Contiene el nombre del usuario de la cuenta. |
| `empresa` | string | Contiene el nombre de la empresa a la que pertenece el prospecto. |
| `fase` | string | Alamacena la descripción de la fase asociada a la oportunidad. |
| `fechaHora` | date | Contiene un formato de fecha compuesto que indica cuando se creó la oportunidad. |
| `fechaProximoRecordatorio` | date | Contiene un formato de fecha compuesto que indica un recordatorio asociado a la oportunidad. |
| `fechaUltimoSeguimiento` | date | Contiene un formato de fecha compuesto que indica cuando se realizó el último seguimiento a la oportunidad. |
| `ganada` | string | Indica si la oportunidad fue convertida en venta. |
| `ganadaFecha` | date | Contiene un formato compuesto de fecha y hora que indica cuando la oportunidad se concretó. |
| `impuestos` | number | Indica un monto monetario que corresponde al importe de impuestos de una oportunidad. |
| `impuestosRetenidos` | number | Indica una cantidad monetaria que corresponde a un importe de inpuestos retenidos.. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `iniciales` | string | Contiene las iniciales del nombre del usuario asociado a la oportunidad. |
| `lineaProducto` | string | Contiene la línea de productos a la cual se encuentra asociada la oportunidad. |
| `moneda` | string | Contiene un código de tres carácteres que indica el tipo de moneda utilizada. |
| `monto` | number | Contiene una cantidad monetaria que corresonde a un monto. |
| `montoPagado` | number | Contiene un monto que determina una cantidad monetaria a cubrir por el prospecto. |
| `perdida` | number | Contiene un código que indica si la oportunidad fue perdida.  - 0 Oportunidad no perdida.  - 1 Oportunidad perdida. |
| `perdidaFecha` | string | Contiene un formato de fecha compuesto que indica cuando ocurró la pérdida. |
| `perdidaRazon` | string | Contiene una razón que describe el motivo por el cual se realizó la pérdida. |
| `tieneProductos` | number | Indica si el prospecto tiene asociado productos. |
| `tipoDeCambio` | number | Contiene un código que define un tipo de cambio con respecto a la moneda nacional. |
| `tkCerteza` | string | Código token que corresponde e identifica la certeza de la oportunidad. |
| `tkFase` | string | Código token que corresponde e identifica de forma única a una fase en el sistema. |
| `tkOportunidad` | string | Código token que corresponde e identifica de forma única a una oportunidad en el sistema. |
| `tkProspecto` | string | Código token que corresponde e identifica de forma única a un prospecto en el sistema. |
| `tkSeguimiento` | string | Código token que corresponde e identifica de forma única a un tipo de seguimiento en el sistema. |
| `tkUsuario` | string | Código token que corresponde e identifica de forma única a un usuario en el sistema. |
| `ultimaModificacion` | date | Contiene un formato de fecha y hora compuesto que indica cuando se realizó la última modificación de la oportunidad. |
| `ultimoContactoComentario` | string | Contiene el comentario del último contacto. |
| `ultimoContactoEjecutivo` | string | Contiene el nombre del ejecutivo que realizó el último contacto. |
| `ultimoContactoFechaHora` | date | Contiene un formato de fecha compuesto que indica cuando se le contactó por última vez. |
| `ultimoContactoIniciales` | string | Contiene las iniciales del ejecutivo que realizó el último contacto. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/prospectos/:tkProspecto/oportunidades` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-prospect-opportunities.md) for the provider-specific parameters and requirements.

