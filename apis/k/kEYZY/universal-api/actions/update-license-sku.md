# KEYZY: Update License SKU

Updates the connected SKU for a KEYZY license.

```
PUT https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-license-sku
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KEYZY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-license-sku" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "currentSkuNumber": "string",
  "newSkuNumber": "string",
  "serial": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/update-license-sku', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "currentSkuNumber": "string",
    "newSkuNumber": "string",
    "serial": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentSkuNumber` | string | yes | Current SKU number. |
| `newSkuNumber` | string | yes | New SKU number. |
| `serial` | string | yes | License serial number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | License update confirmation message. |

## Native endpoint

Through the native KEYZY API, this operation is `POST /licenses/update-sku` (base URL `https://api.keyzy.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-license-sku.md) for the provider-specific parameters and requirements.

