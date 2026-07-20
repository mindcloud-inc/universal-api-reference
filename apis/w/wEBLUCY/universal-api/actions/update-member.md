# WEBLUCY: Update Member

Updates an existing member in WEBLUCY.

```
PUT https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/update-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `approved` | boolean | no | Whether the member is approved. |
| `id` | string | yes | The member ID. |
| `name` | string | no | The member name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "billingAddress": {},
      "contactId": 1,
      "email": "ava@example.com",
      "extra": {},
      "groups": [
        1
      ],
      "id": 1,
      "name": "Ava Chen",
      "password": "string",
      "registeredOn": 1,
      "shippingAddress": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `billingAddress` | object |  |
| `contactId` | number |  |
| `email` | string |  |
| `extra` | object |  |
| `groups` | array<number> |  |
| `id` | number |  |
| `name` | string |  |
| `password` | string |  |
| `registeredOn` | number |  |
| `shippingAddress` | object |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `PUT /members/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-member.md) for the provider-specific parameters and requirements.

