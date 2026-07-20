# ThingsBoard: Save Customer

Creates or updates a customer in ThingsBoard.

```
PUT https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/save-customer', {
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
      "city": "string",
      "country": "string",
      "createdTime": 1,
      "email": "ava@example.com",
      "id": {
        "entityType": "string",
        "id": "string"
      },
      "phone": "string",
      "tenantId": {
        "id": "string"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `createdTime` | number |  |
| `email` | string |  |
| `id.entityType` | string |  |
| `id.id` | string |  |
| `phone` | string |  |
| `tenantId.id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native ThingsBoard API, this operation is `POST /customer` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-customer.md) for the provider-specific parameters and requirements.

