# Buy Me a Coffee: List Extra Purchases

Retrieves extra purchases from Buy Me a Coffee.

```
GET https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-extra-purchases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buy Me a Coffee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-extra-purchases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-extra-purchases?${params}`, {
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
          "extra": {
            "rewardCoffeePrice": "string",
            "rewardConfirmationMessage": "string",
            "rewardCreatedOn": "2026-05-07T12:00:00.000Z",
            "rewardDeletedOn": "2026-05-07T12:00:00.000Z",
            "rewardDescription": "string",
            "rewardId": 1,
            "rewardImage": "string",
            "rewardIsActive": 1,
            "rewardOrder": 1,
            "rewardQuestion": "string",
            "rewardSlots": 1,
            "rewardTitle": "string",
            "rewardUpdatedOn": "2026-05-07T12:00:00.000Z",
            "rewardUsed": 1
          },
          "payerEmail": "ava@example.com",
          "payerName": "Ava Chen",
          "purchaseAmount": "string",
          "purchaseCurrency": "string",
          "purchasedOn": "2026-05-07T12:00:00.000Z",
          "purchaseId": 1,
          "purchaseIsRevoked": 1,
          "purchaseQuestion": "string",
          "purchaseUpdatedOn": "2026-05-07T12:00:00.000Z",
          "totalPaidAmount": "string"
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
| `data[].extra` | object |  |
| `data[].extra.rewardCoffeePrice` | string |  |
| `data[].extra.rewardConfirmationMessage` | string |  |
| `data[].extra.rewardCreatedOn` | date |  |
| `data[].extra.rewardDeletedOn` | date |  |
| `data[].extra.rewardDescription` | string |  |
| `data[].extra.rewardId` | number |  |
| `data[].extra.rewardImage` | string |  |
| `data[].extra.rewardIsActive` | number |  |
| `data[].extra.rewardOrder` | number |  |
| `data[].extra.rewardQuestion` | string |  |
| `data[].extra.rewardSlots` | number |  |
| `data[].extra.rewardTitle` | string |  |
| `data[].extra.rewardUpdatedOn` | date |  |
| `data[].extra.rewardUsed` | number |  |
| `data[].payerEmail` | string |  |
| `data[].payerName` | string |  |
| `data[].purchaseAmount` | string |  |
| `data[].purchaseCurrency` | string |  |
| `data[].purchasedOn` | date |  |
| `data[].purchaseId` | number |  |
| `data[].purchaseIsRevoked` | number |  |
| `data[].purchaseQuestion` | string |  |
| `data[].purchaseUpdatedOn` | date |  |
| `data[].totalPaidAmount` | string |  |
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

Through the native Buy Me a Coffee API, this operation is `GET /extras` (base URL `https://developers.buymeacoffee.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-extra-purchases.md) for the provider-specific parameters and requirements.

