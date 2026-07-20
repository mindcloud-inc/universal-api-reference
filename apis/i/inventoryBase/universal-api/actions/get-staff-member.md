# InventoryBase: Get Staff Member

Retrieves a staff member from InventoryBase by ID.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-staff-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-staff-member?connectionId=$CONNECTION_ID&staffId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "staffId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-staff-member?${params}`, {
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
| `staffId` | number | yes | The InventoryBase staff member ID. |

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
      "availabilityLocation": {},
      "company": "string",
      "customFields": {},
      "disabledTypes": [
        "string"
      ],
      "email": "ava@example.com",
      "emailNotifications": 1,
      "id": 1,
      "isAdminManager": true,
      "isManager": true,
      "isTypist": true,
      "lastLogin": "string",
      "loginEnabled": true,
      "name": "Ava Chen",
      "role": 1,
      "settings": {},
      "team": {},
      "telephone": "string",
      "twoFactorEnabled": true
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
| `availabilityLocation` | object |  |
| `company` | string |  |
| `customFields` | object |  |
| `disabledTypes` | array<string> |  |
| `email` | string |  |
| `emailNotifications` | number |  |
| `id` | number |  |
| `isAdminManager` | boolean |  |
| `isManager` | boolean |  |
| `isTypist` | boolean |  |
| `lastLogin` | string |  |
| `loginEnabled` | boolean |  |
| `name` | string |  |
| `role` | number |  |
| `settings` | object |  |
| `team` | object |  |
| `telephone` | string |  |
| `twoFactorEnabled` | boolean |  |

## Native endpoint

Through the native InventoryBase API, this operation is `GET /staff/:staffId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-staff-member.md) for the provider-specific parameters and requirements.

