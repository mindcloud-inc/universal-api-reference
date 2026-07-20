# Print.one Postcards: List Batches

Retrieves batches from Print.one Postcards.

```
GET https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Print.one Postcards `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-batches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printonePostcards/latest/actions/list-batches?${params}`, {
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "billingId": "string",
      "companyId": "string",
      "countryId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expectedDeliveryTimeframe": [
        "2026-05-07T12:00:00.000Z"
      ],
      "finish": "string",
      "format": "string",
      "id": "string",
      "isBillable": true,
      "name": "Ava Chen",
      "orders": {},
      "requiredCount": 1,
      "sendDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "templateId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedAt` | date |  |
| `billingId` | string |  |
| `companyId` | string |  |
| `countryId` | string |  |
| `createdAt` | date |  |
| `expectedDeliveryTimeframe` | array<date> |  |
| `finish` | string |  |
| `format` | string |  |
| `id` | string |  |
| `isBillable` | boolean |  |
| `name` | string |  |
| `orders` | object |  |
| `requiredCount` | number |  |
| `sendDate` | date |  |
| `status` | string |  |
| `templateId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Print.one Postcards API, this operation is `GET /v2/batches` (base URL `https://api.print.one`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batches.md) for the provider-specific parameters and requirements.

