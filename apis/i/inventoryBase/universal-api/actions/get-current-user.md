# InventoryBase: Get Current User

Retrieves the current user profile from InventoryBase.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-current-user?${params}`, {
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
      "accountId": 1,
      "accountSettings": {},
      "company": "string",
      "currencyCode": "string",
      "currencySymbol": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "role": 1,
      "signature": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `accountSettings` | object |  |
| `company` | string |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `role` | number |  |
| `signature` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `GET /me` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

