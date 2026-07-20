# Tarvent: List Transactions

Retrieves transactions from Tarvent.

```
GET https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tarvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tarvent/latest/actions/list-transactions?${params}`, {
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
      "bounceCategory": "string",
      "clickCount": 1,
      "complaint": true,
      "contactId": "string",
      "createdUtc": "2026-05-07T12:00:00.000Z",
      "device": "string",
      "enableAnalytics": true,
      "enableViewOnline": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounceCategory` | string |  |
| `clickCount` | number |  |
| `complaint` | boolean |  |
| `contactId` | string |  |
| `createdUtc` | date |  |
| `device` | string |  |
| `enableAnalytics` | boolean |  |
| `enableViewOnline` | boolean |  |

## Native endpoint

Through the native Tarvent API, this operation is `POST /graphql` (base URL `https://api.tarvent.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

