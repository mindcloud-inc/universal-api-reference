# Modern Treasury: List Transaction Line Items

Retrieves transaction line items from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-transaction-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-transaction-line-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-transaction-line-items?${params}`, {
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
      "amount": 1,
      "counterpartyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "discardedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "liveMode": true,
      "object": "string",
      "transactableId": "string",
      "transactableType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `counterpartyId` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `discardedAt` | date |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `object` | string |  |
| `transactableId` | string |  |
| `transactableType` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /transaction_line_items` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transaction-line-items.md) for the provider-specific parameters and requirements.

