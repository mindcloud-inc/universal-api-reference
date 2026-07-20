# EenvoudigFactureren: Update Client

Updates an existing client in EenvoudigFactureren.

```
PUT https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "client_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "client_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `client_id` | string | yes | EenvoudigFactureren client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "client_id": 1,
      "country": "string",
      "email_address": "ava@example.com",
      "last_activity": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "number": "string",
      "phone_number": "string",
      "postal_code": "string",
      "state": "string",
      "street": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `client_id` | number |  |
| `country` | string |  |
| `email_address` | string |  |
| `last_activity` | date |  |
| `name` | string |  |
| `number` | string |  |
| `phone_number` | string |  |
| `postal_code` | string |  |
| `state` | string |  |
| `street` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `PUT /clients/:client_id` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

