# Formstack Documents: Create Data Route Delivery

Creates a data route delivery in Formstack Documents.

```
POST https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-data-route-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formstack Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-data-route-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/create-data-route-delivery', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ID of the data route to create a delivery for |
| `settings.from` | string | no | Sender address for email deliveries |
| `settings.html` | string | no | HTML body for email deliveries |
| `settings.subject` | string | no | Subject for email deliveries |
| `settings.to` | string | no | Recipient value for email deliveries |
| `type` | string | yes | Delivery type such as email or webhook |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "settings": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `settings` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Formstack Documents API, this operation is `POST /routes/:id/deliveries` (base URL `https://www.webmerge.me/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-data-route-delivery.md) for the provider-specific parameters and requirements.

