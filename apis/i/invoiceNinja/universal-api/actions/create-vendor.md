# Invoice Ninja: Create Vendor



```
POST https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-vendor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/create-vendor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The vendor name. |
| `email` | string | no | Primary vendor email. |
| `phone` | string | no | Primary vendor phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": 1,
      "contacts": [
        {}
      ],
      "countryId": "string",
      "createdAt": 1,
      "currencyId": "string",
      "displayName": "Ava Chen",
      "documents": [
        {}
      ],
      "id": "string",
      "isDeleted": true,
      "name": "Ava Chen",
      "number": "string",
      "phone": "string",
      "privateNotes": "string",
      "publicNotes": "string",
      "updatedAt": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | number |  |
| `contacts` | array<object> |  |
| `countryId` | string |  |
| `createdAt` | number |  |
| `currencyId` | string |  |
| `displayName` | string |  |
| `documents` | array<object> |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `name` | string |  |
| `number` | string |  |
| `phone` | string |  |
| `privateNotes` | string |  |
| `publicNotes` | string |  |
| `updatedAt` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `POST /vendors` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vendor.md) for the provider-specific parameters and requirements.

