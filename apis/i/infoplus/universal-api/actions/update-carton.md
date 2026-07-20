# Infoplus: Update Carton

Updates an existing carton in Infoplus.

```
PUT https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-carton
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infoplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-carton" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infoplus/latest/actions/update-carton', {
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
      "cartonLPN": "string",
      "cartonNo": 1,
      "id": 1,
      "lobId": 1,
      "orderNo": 1,
      "weightLbs": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartonLPN` | string |  |
| `cartonNo` | number |  |
| `id` | number |  |
| `lobId` | number |  |
| `orderNo` | number |  |
| `weightLbs` | number |  |

## Native endpoint

Through the native Infoplus API, this operation is `PUT /carton` (base URL `https://luxomo.infopluswms.com/infoplus-wms/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-carton.md) for the provider-specific parameters and requirements.

