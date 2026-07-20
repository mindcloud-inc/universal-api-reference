# Easyship: List Shipping Rules

Retrieves a list of shipping rules from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipping-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipping-rules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipping-rules?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accessible": true,
      "active": true,
      "checkoutRestrictive": true,
      "createdAt": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "priority": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessible` | boolean |  |
| `active` | boolean |  |
| `checkoutRestrictive` | boolean |  |
| `createdAt` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `priority` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /shipping_rules` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipping-rules.md) for the provider-specific parameters and requirements.

