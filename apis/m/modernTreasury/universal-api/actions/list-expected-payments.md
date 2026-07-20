# Modern Treasury: List Expected Payments

Retrieves expected payments from Modern Treasury.

```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-expected-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-expected-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-expected-payments?${params}`, {
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
      "amountLowerBound": 1,
      "amountUpperBound": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "direction": "string",
      "externalId": "string",
      "id": "string",
      "internalAccountId": "string",
      "liveMode": true,
      "object": "string",
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
| `amountLowerBound` | number |  |
| `amountUpperBound` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `direction` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `internalAccountId` | string |  |
| `liveMode` | boolean |  |
| `object` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /expected_payments` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-expected-payments.md) for the provider-specific parameters and requirements.

