# Invoice Ninja: List Vendors



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-vendors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-vendors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-vendors?${params}`, {
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

Through the native Invoice Ninja API, this operation is `GET /vendors` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vendors.md) for the provider-specific parameters and requirements.

