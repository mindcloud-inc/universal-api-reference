# Open Data DC: Create SSL Lookup By Identifier



```
POST https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-ssl-lookup-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Data DC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-ssl-lookup-by-identifier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ssl": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openDataDC/latest/actions/create-ssl-lookup-by-identifier', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ssl": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ssl` | string | yes | Square, suffix, lot identifier. |

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

Through the native Open Data DC API, this operation is `POST /api/v2.2/ssls/:ssl` (base URL `https://datagate.dc.gov/mar/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ssl-lookup-by-identifier.md) for the provider-specific parameters and requirements.

