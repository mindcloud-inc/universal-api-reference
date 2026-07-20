# Upnify: List Opportunity Products

Retrieves products for an opportunity in Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-opportunity-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-opportunity-products?connectionId=$CONNECTION_ID&tkOportunidad=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkOportunidad": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-opportunity-products?${params}`, {
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
| `tkOportunidad` | string | yes | El Identificador unico de una oportunidad dentro del CRM, de la cual se requiere conocer la lista de productos asociados. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campoPersonalizadoProducto1": "string",
      "cantidad": 1,
      "codigo": "string",
      "comentario": "string",
      "comision": 1,
      "comisionMonto": 1,
      "costo": 1,
      "descripcion1": "string",
      "descripcion2": "string",
      "descripcionCorta": "string",
      "descuento": 1,
      "descuentoPct": 1,
      "descuentoUnitario": 1,
      "existencia": 1,
      "fechaFin": "2026-05-07T12:00:00.000Z",
      "fechaInicio": "2026-05-07T12:00:00.000Z",
      "idMoneda": "string",
      "imagenes": {},
      "impEmpresa": {},
      "impuesto1": 1,
      "impuestoR1": 1,
      "indice": 1,
      "indiceComision": 1,
      "linea": "string",
      "link": "https://example.com",
      "listaPrecio": "string",
      "marca": "string",
      "modelo": "string",
      "monto": 1,
      "noches": 1,
      "precio1": 1,
      "precioMin": 1,
      "producto": "string",
      "productoPrecio": 1,
      "status": 1,
      "subtotal": 1,
      "subtotalImpuestos": 1,
      "tipoDeCambio": 1,
      "tkLineaProducto": "string",
      "tkListaPrecio": "string",
      "tkMaestro": "string",
      "tkMarca": "string",
      "tkModelo": "string",
      "tkMoneda": "string",
      "tkProducto": "string",
      "unidad": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campoPersonalizadoProducto1` | string | Campo personalizado para el caso de los productos, se puede tener hasta 30. |
| `cantidad` | number | Cantidad de productos seleccionados para la cotizacion. |
| `codigo` | string | Contiene un código establecido por el usuario para identificar el producto dentro el sistema. |
| `comentario` | string | Se guarda un comentario que corresponde a los productos seleccionados. |
| `comision` | number | Indica una cantidad de comision con base 1, (donde 1 es el 100%)por el producto. |
| `comisionMonto` | number | Contiene un monto monetario correspondiente a la comision por el producto. |
| `costo` | number | Guarda el costo base del producto. |
| `descripcion1` | string | Descripción completa del producto. |
| `descripcion2` | string | Almacena una segunda descripción del producto. |
| `descripcionCorta` | string | Descripción del producto que tiene un número límite de carácteres. |
| `descuento` | number | Guarda el monto de descuento. |
| `descuentoPct` | number | Indica una cantidad de descuento con base 1, (donde 1 es el 100%), aplicable a los productos seleccionados. |
| `descuentoUnitario` | number | Almacena una catidad que representa un porcentaje para calcular un descuento. |
| `existencia` | number | Indica la cantidad de productos disponibles en inventario. |
| `fechaFin` | date | Contiene un formato de fecha que indica el final de noches en las que se hospedaran los clientes |
| `fechaInicio` | date | Contiene un formato de fecha que indica el inicio de noches en las que se hospedaran los clientes |
| `idMoneda` | string | Indica el codigo de la moneda dependiendo del país. |
| `imagenes` | object | contiene un arreglo de datos donde se guarda la información de hasta diez imágenes que se asocian al producto. |
| `impEmpresa` | object | Contiene un arreglo de datos que indican los tipos de impuesto que actualmente utiliza la empresa para el producto. |
| `impuesto1` | number | Guarda un valor de tipo de impuesto que se puede aplicar al producto, pueden existir hasta diez valores de impuestos. |
| `impuestoR1` | number | ALmacena un valor de tipo de impuesto retenido que se puede aplicar al producto, pueden existir hasta diez valores de impuestos. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `indiceComision` | number | Contiene un número que indica un indice de comisión. |
| `linea` | string | Indica a que línea de productos pertenece el producto. |
| `link` | string | ALmacena la dirección o la ruta en donde se guardan los adjuntos del producto. |
| `listaPrecio` | string | Guarda el nombre de la lista de precio acorrespondiente al producto de la cotizacion. |
| `marca` | string | Guarda la marca comercial del producto. |
| `modelo` | string | Guarda el modelo del producto. |
| `monto` | number | Coste total de los productos seleccionados. |
| `noches` | number | Guarda el numero total de noches que los clientes se hospedaran. |
| `precio1` | number | Contiene un costo adicional del producto, se pueden tener hasta diez precios diferentes. |
| `precioMin` | number | Contiene un precio mínimo de venta del producto, no puede ser menor al costo. |
| `producto` | string | Contiene el nombre de un producto registrado en sistema. |
| `productoPrecio` | number | Guarda el precio unitario de los productos. |
| `status` | number | Código que indica si el producto se encuentra actualmente disponible o no.  - 0 Producto no disponible.  - 1 Producto disponible. |
| `subtotal` | number | Coste de los productos seleccionados sin impuestos o descuentos. |
| `subtotalImpuestos` | number | Contiene el subtotal de los impuestos aplicables. |
| `tipoDeCambio` | number | Indica el valor de la moneda utilizada, con respecto a la moneda nacional. |
| `tkLineaProducto` | string | Identificador unico de una línea de productos dentro el sistema. |
| `tkListaPrecio` | string | Identificador unico de una lista de precio dentro el sistema. |
| `tkMaestro` | string | Identificador unico que es utilizado cuando un producto se encuentra compartido. |
| `tkMarca` | string | Identificador unico de una marca dentro el sistema. |
| `tkModelo` | string | Identificador unico de un modelo dentro el sistema. |
| `tkMoneda` | string | Identificador unico de una moneda dentro el sistema. |
| `tkProducto` | string | Identificador unico de un producto dentro el sistema. |
| `unidad` | string | Contiene la unidad de contabilización del producto. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/oportunidades/:tkOportunidad/productos` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-opportunity-products.md) for the provider-specific parameters and requirements.

