# WEBLUCY: Get Member

Retrieves a member from WEBLUCY.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-member?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/get-member?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The member ID. |

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

Through the native WEBLUCY API, this operation is `GET /members/{id}` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-member.md) for the provider-specific parameters and requirements.

