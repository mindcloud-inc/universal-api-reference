# Turis: List Orders

Retrieves orders from Turis.

```
GET https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-orders?${params}`, {
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
      "casesCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "itemsCount": 1,
      "recEquiv": 1,
      "showRecEquiv": true,
      "status": "string",
      "type": "string",
      "uniqueId6": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `casesCount` | number |  |
| `createdAt` | date |  |
| `id` | number |  |
| `itemsCount` | number |  |
| `recEquiv` | number |  |
| `showRecEquiv` | boolean |  |
| `status` | string |  |
| `type` | string |  |
| `uniqueId6` | string |  |
| `vat` | number |  |

## Native endpoint

Through the native Turis API, this operation is `GET /api/public/v1/orders` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

