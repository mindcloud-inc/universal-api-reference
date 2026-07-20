# Modern Treasury: List Account Collection Flows

Retrieves account collection flows from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-account-collection-flows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-account-collection-flows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-account-collection-flows?${params}`, {
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
      "clientToken": "string",
      "counterpartyId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "externalAccountId": "string",
      "id": "string",
      "liveMode": true,
      "object": "string",
      "paymentTypes": [
        "string"
      ],
      "receivingCountries": [
        "string"
      ],
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientToken` | string |  |
| `counterpartyId` | string |  |
| `createdAt` | date |  |
| `externalAccountId` | string |  |
| `id` | string |  |
| `liveMode` | boolean |  |
| `object` | string |  |
| `paymentTypes` | array<string> |  |
| `receivingCountries` | array<string> |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /account_collection_flows` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-collection-flows.md) for the provider-specific parameters and requirements.

