# WEBLUCY: Create Member

Creates a new member in WEBLUCY.

```
POST https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/create-member', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The member email address. |
| `name` | string | yes | The member name. |
| `password` | string | yes | The member password. If omitted, WEBLUCY sends a password reset email instead. |

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

Through the native WEBLUCY API, this operation is `POST /members` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-member.md) for the provider-specific parameters and requirements.

