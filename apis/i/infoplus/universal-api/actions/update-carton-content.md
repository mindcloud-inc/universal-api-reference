# Infoplus: Update Carton Content

Updates an existing carton content in Infoplus.

```
PUT https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-carton-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-carton-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-carton-content', {
  method: 'PUT',
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
      "cartonId": 1,
      "cartonNo": 1,
      "id": 1,
      "quantity": 1,
      "sku": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartonId` | number |  |
| `cartonNo` | number |  |
| `id` | number |  |
| `quantity` | number |  |
| `sku` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Infoplus API, this operation is `PUT /cartonContent` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-carton-content.md) for the provider-specific parameters and requirements.

