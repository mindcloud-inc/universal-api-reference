# InventoryBase: Get Client

Retrieves a client from InventoryBase by ID.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-client?${params}`, {
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
| `clientId` | number | yes | The InventoryBase client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {
        "city": "string",
        "line1": "string",
        "postcode": "string"
      },
      "company": "string",
      "createdAt": "string",
      "customFields": {},
      "disabledTypes": [
        "string"
      ],
      "email": "ava@example.com",
      "emailNotifications": true,
      "id": 1,
      "isAdminManager": true,
      "isManager": true,
      "isTypist": true,
      "loginEnabled": true,
      "name": "Ava Chen",
      "role": 1,
      "settings": {},
      "telephone": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `address.city` | string |  |
| `address.line1` | string |  |
| `address.postcode` | string |  |
| `company` | string |  |
| `createdAt` | string |  |
| `customFields` | object |  |
| `disabledTypes` | array<string> |  |
| `email` | string |  |
| `emailNotifications` | boolean |  |
| `id` | number |  |
| `isAdminManager` | boolean |  |
| `isManager` | boolean |  |
| `isTypist` | boolean |  |
| `loginEnabled` | boolean |  |
| `name` | string |  |
| `role` | number |  |
| `settings` | object |  |
| `telephone` | string |  |
| `website` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `GET /clients/:clientId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

