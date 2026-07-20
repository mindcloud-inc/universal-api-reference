# Open Data DC: Create SSL Lookup



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-ssl-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-ssl-lookup" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-ssl-lookup', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "FullAddress": "string",
      "Lot": "string",
      "MarId": "string",
      "Square": "string",
      "SSL": "string",
      "Suffix": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `FullAddress` | string | Full address. |
| `Lot` | string | Lot. |
| `MarId` | string | MAR identifier. |
| `Square` | string | Square. |
| `SSL` | string | Square, suffix, lot. |
| `Suffix` | string | Suffix. |

## Native endpoint

Through the native Open Data DC API, this operation is `POST /api/v2.2/ssls` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ssl-lookup.md) for the provider-specific parameters and requirements.

