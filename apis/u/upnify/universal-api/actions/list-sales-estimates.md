# Upnify: List Sales Estimates

Retrieves sales estimates from Upnify.

```
GET https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sales-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Upnify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sales-estimates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upnify/latest/actions/list-sales-estimates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "comisionMonto": 1,
      "conteo": 1,
      "indice": 1,
      "monto": 1,
      "probabilidad": 1,
      "promedioCerteza": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comisionMonto` | number | Contiene el monto de la comision. |
| `conteo` | number | Contiene el numero de oportunidades del cliente. |
| `indice` | number | Define la posición del registro respecto a los demás registros. |
| `monto` | number | Guarda el monto de venta. |
| `probabilidad` | number | Indica la probabilidad de que el cliente compre. |
| `promedioCerteza` | number | Contiene el promedio de la certeza del cliente. |

## Native endpoint

Through the native Upnify API, this operation is `GET v4/oportunidades/estimacion` (base URL `https://api.upnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sales-estimates.md) for the provider-specific parameters and requirements.

