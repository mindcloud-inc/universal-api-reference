# Modern Treasury: List Foreign Exchange Quotes



```
GET https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-foreign-exchange-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modern Treasury `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-foreign-exchange-quotes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modernTreasury/latest/actions/list-foreign-exchange-quotes?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "effectiveAt": "2026-05-07T12:00:00.000Z",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "foreignExchangeIndicator": "string",
      "foreignExchangeRate": "string",
      "id": "string",
      "internalAccountId": "string",
      "liveMode": true,
      "metadata": {},
      "object": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `effectiveAt` | date |  |
| `expiresAt` | date |  |
| `foreignExchangeIndicator` | string |  |
| `foreignExchangeRate` | string |  |
| `id` | string |  |
| `internalAccountId` | string |  |
| `liveMode` | boolean |  |
| `metadata` | object |  |
| `object` | string |  |
| `updatedAt` | date |  |
| `vendorId` | string |  |

## Native endpoint

Through the native Modern Treasury API, this operation is `GET /foreign_exchange_quotes` (base URL `https://app.moderntreasury.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-foreign-exchange-quotes.md) for the provider-specific parameters and requirements.

