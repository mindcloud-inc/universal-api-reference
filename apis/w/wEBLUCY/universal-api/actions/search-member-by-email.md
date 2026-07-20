# WEBLUCY: Search Member by Email

Finds members in WEBLUCY by email address.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/search-member-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/search-member-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/search-member-by-email?${params}`, {
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
| `email` | string | yes | The member email address to search for. |

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

Through the native WEBLUCY API, this operation is `GET /members/search-by-email` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-member-by-email.md) for the provider-specific parameters and requirements.

