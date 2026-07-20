# InventoryBase: Create Client

Creates a new client in InventoryBase.

```
POST https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "address": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "address": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The client's full name. |
| `email` | string | yes | The client's email address. |
| `address` | object | yes | The client's primary address object. |
| `telephone` | string | no | The client's telephone number. |
| `company` | string | no | The client's company name. |
| `website` | string | no | The client's website. |
| `notes` | string | no | Notes about the client. |
| `sendLoginDetails` | boolean | no | Whether to send login details to the new client. |
| `emailNotifications` | boolean | no | Whether the client should receive email notifications. |
| `ignoreWelcomeMailer` | boolean | no | Whether to suppress the initial welcome email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalEmails": [
        "ava@example.com"
      ],
      "address": {
        "city": "string",
        "country": "string",
        "county": "string",
        "line1": "string",
        "line2": "string",
        "postcode": "string"
      },
      "billingEmail": "ava@example.com",
      "company": "string",
      "companyNo": "string",
      "createdAt": "string",
      "customFields": {},
      "deletedAt": "string",
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
      "logo": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "pendingEmail": "ava@example.com",
      "role": 1,
      "settings": {},
      "signature": "string",
      "telephone": "string",
      "title": "string",
      "vatNo": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalEmails` | array<string> |  |
| `address` | object |  |
| `address.city` | string |  |
| `address.country` | string |  |
| `address.county` | string |  |
| `address.line1` | string |  |
| `address.line2` | string |  |
| `address.postcode` | string |  |
| `billingEmail` | string |  |
| `company` | string |  |
| `companyNo` | string |  |
| `createdAt` | string |  |
| `customFields` | object |  |
| `deletedAt` | string |  |
| `disabledTypes` | array<string> |  |
| `email` | string |  |
| `emailNotifications` | boolean |  |
| `id` | number |  |
| `isAdminManager` | boolean |  |
| `isManager` | boolean |  |
| `isTypist` | boolean |  |
| `loginEnabled` | boolean |  |
| `logo` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `pendingEmail` | string |  |
| `role` | number |  |
| `settings` | object |  |
| `signature` | string |  |
| `telephone` | string |  |
| `title` | string |  |
| `vatNo` | string |  |
| `website` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `POST /clients` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

