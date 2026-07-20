# CustomerX: Update Contact By External ID

Updates an existing contact in CustomerX by external ID.

```
PUT https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-contact-by-external-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-contact-by-external-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customerX/latest/actions/update-contact-by-external-id', {
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
      "birthday": "string",
      "client": {},
      "client_id": 1,
      "created_at": "string",
      "email": "ava@example.com",
      "external_id_contact": "string",
      "id": 1,
      "is_principal": true,
      "name": "Ava Chen",
      "occupation": "string",
      "phone_cel": "string",
      "phone_fix": "string",
      "phones": [
        {}
      ],
      "type_contact": {},
      "type_contact_id": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string |  |
| `client` | object |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `email` | string |  |
| `external_id_contact` | string |  |
| `id` | number |  |
| `is_principal` | boolean |  |
| `name` | string |  |
| `occupation` | string |  |
| `phone_cel` | string |  |
| `phone_fix` | string |  |
| `phones` | array<object> |  |
| `type_contact` | object |  |
| `type_contact_id` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `PUT /api/v1/contacts` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-by-external-id.md) for the provider-specific parameters and requirements.

