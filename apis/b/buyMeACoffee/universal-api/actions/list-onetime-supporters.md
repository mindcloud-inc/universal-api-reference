# Buy Me a Coffee: List Onetime Supporters

Retrieves onetime supporters from Buy Me a Coffee.

```
GET https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-onetime-supporters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buy Me a Coffee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-onetime-supporters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-onetime-supporters?${params}`, {
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
      "currentPage": 1,
      "data": [
        {
          "country": "string",
          "isRefunded": true,
          "payerEmail": "ava@example.com",
          "payerName": "Ava Chen",
          "paymentPlatform": "string",
          "referer": "string",
          "supportCoffeePrice": "string",
          "supportCoffees": 1,
          "supportCreatedOn": "2026-05-07T12:00:00.000Z",
          "supportCurrency": "string",
          "supportEmail": "ava@example.com",
          "supporterName": "Ava Chen",
          "supportId": 1,
          "supportNote": "string",
          "supportNotePinned": 1,
          "supportUpdatedOn": "2026-05-07T12:00:00.000Z",
          "supportVisibility": 1,
          "transactionId": "string",
          "transferId": "string"
        }
      ],
      "firstPageUrl": "https://example.com",
      "from": 1,
      "lastPage": 1,
      "lastPageUrl": "https://example.com",
      "nextPageUrl": "https://example.com",
      "path": "string",
      "perPage": 1,
      "prevPageUrl": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].country` | string |  |
| `data[].isRefunded` | boolean |  |
| `data[].payerEmail` | string |  |
| `data[].payerName` | string |  |
| `data[].paymentPlatform` | string |  |
| `data[].referer` | string |  |
| `data[].supportCoffeePrice` | string |  |
| `data[].supportCoffees` | number |  |
| `data[].supportCreatedOn` | date |  |
| `data[].supportCurrency` | string |  |
| `data[].supportEmail` | string |  |
| `data[].supporterName` | string |  |
| `data[].supportId` | number |  |
| `data[].supportNote` | string |  |
| `data[].supportNotePinned` | number |  |
| `data[].supportUpdatedOn` | date |  |
| `data[].supportVisibility` | number |  |
| `data[].transactionId` | string |  |
| `data[].transferId` | string |  |
| `firstPageUrl` | string |  |
| `from` | number |  |
| `lastPage` | number |  |
| `lastPageUrl` | string |  |
| `nextPageUrl` | string |  |
| `path` | string |  |
| `perPage` | number |  |
| `prevPageUrl` | string |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Buy Me a Coffee API, this operation is `GET /supporters` (base URL `https://developers.buymeacoffee.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-onetime-supporters.md) for the provider-specific parameters and requirements.

