# Upnify: Get Product

Retrieves a product from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-product?connectionId=$CONNECTION_ID&tkProducto=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tkProducto": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/get-product?${params}`, {
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
| `tkProducto` | string | yes | El token que identifica a un producto en el sistema, del cual se requiere obtener los detalles. ¿Dónde obtengo el token? |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bloqueado": true,
      "claveProductoServicio": "string",
      "claveUnidad": "string",
      "codigo": "string",
      "comision1": 1,
      "comision10": 1,
      "costo": 1,
      "descripcionCvp": "string",
      "existencia": "string",
      "imagenes": "string",
      "impuesto1": 1,
      "impuesto10": 1,
      "impuestoRetenido1": 1,
      "impuestoRetenido10": 1,
      "indice": 1,
      "lineaProducto": "string",
      "link": "https://example.com",
      "marca": "string",
      "nombre": "string",
      "nombreUni": "string",
      "precio1": 1,
      "precio10": 1,
      "precioMinimo": 1,
      "status": 1,
      "statusTexto": "string",
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
| `bloqueado` | boolean |  |
| `claveProductoServicio` | string | Almacena una clave de producto o servicio, seleccionado del catálogo de productos del SAT. |
| `claveUnidad` | string | Almacena una clave de unidad, seleccionado del catálogo de medidas del SAT. |
| `codigo` | string | Contiene un código que puede ser establecido por el usuario para poder identificar el producto en el sistema. |
| `comision1` | number | Guarda la comision del producto. |
| `comision10` | number | Guarda la comision del producto. |
| `costo` | number | Guarda el costo real del producto. |
| `descripcionCvp` | string | Muestra una descripción de la clave de producto selecionada del catálogo del SAT. |
| `existencia` | string | Guarda la cantidad de productos disponibles. |
| `imagenes` | string | Contiene un arreglo de datos en donde se guarda los datos de hasta diez imágenes que el usuario puede subir, para promosionar el producto. |
| `impuesto1` | number | Guarda el impuesto para el producto. |
| `impuesto10` | number | Guarda el impuesto para el producto. |
| `impuestoRetenido1` | number | Guarda el impuesto retenido para el producto. |
| `impuestoRetenido10` | number | Guarda el impuesto retenido para el producto. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `lineaProducto` | string | Indica a que línea de productos del sistema, pertene el producto. |
| `link` | string | Almacena la dirección del servidor, en donde se almacenaran las imágenes que el usuario establesca para su producto. |
| `marca` | string | Almacena la marca a la que pertenece el producto. |
| `nombre` | string | Guarda el nombre con el que el producto que se registró en el sistema. |
| `nombreUni` | string | Muestra una descripción o nombre del tipo de unidad, seleccionada del catálogo de medidas del SAT. |
| `precio1` | number | Guarda el precio real del producto. |
| `precio10` | number | Guarda el precio real del producto. |
| `precioMinimo` | number | Contiene el costo de venta al público del productom este precio no puede ser menor al costo real del producto. |
| `status` | number | Código que define si el producto se encuentra activo o no en el sistema.  - 0 Inactivo.  - 1 Activo. |
| `statusTexto` | string | Muestra un mensaje que indica el estado de activación del producto. |
| `tkProducto` | string | Código token que identifica de forma única a un prodcuto dentro el sistema. |
| `unidad` | string | Muestra la unidad de medida utilizada para contabilizar el producto. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/catalogos/productos/:tkProducto` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

