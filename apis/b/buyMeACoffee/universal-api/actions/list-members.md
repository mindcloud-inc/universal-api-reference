# Buy Me a Coffee: List Members

Retrieves members from Buy Me a Coffee.

```
GET https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buy Me a Coffee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-members?connectionId=$CONNECTION_ID&status=all" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "status": "all"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/list-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | yes | Filter memberships by status. Official docs allow active, inactive, or all. Default: `all`. |

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
          "messageVisibility": 1,
          "payerEmail": "ava@example.com",
          "payerName": "Ava Chen",
          "referer": "string",
          "subscriptionCancelledOn": "2026-05-07T12:00:00.000Z",
          "subscriptionCoffeeNum": 1,
          "subscriptionCoffeePrice": "string",
          "subscriptionCreatedOn": "2026-05-07T12:00:00.000Z",
          "subscriptionCurrency": "string",
          "subscriptionCurrentPeriodEnd": "2026-05-07T12:00:00.000Z",
          "subscriptionCurrentPeriodStart": "2026-05-07T12:00:00.000Z",
          "subscriptionDurationType": "string",
          "subscriptionId": 1,
          "subscriptionIsCancelled": true,
          "subscriptionIsCancelledAtPeriodEnd": true,
          "subscriptionMessage": "string",
          "subscriptionUpdatedOn": "2026-05-07T12:00:00.000Z",
          "transactionId": "string"
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
| `data[].messageVisibility` | number |  |
| `data[].payerEmail` | string |  |
| `data[].payerName` | string |  |
| `data[].referer` | string |  |
| `data[].subscriptionCancelledOn` | date |  |
| `data[].subscriptionCoffeeNum` | number |  |
| `data[].subscriptionCoffeePrice` | string |  |
| `data[].subscriptionCreatedOn` | date |  |
| `data[].subscriptionCurrency` | string |  |
| `data[].subscriptionCurrentPeriodEnd` | date |  |
| `data[].subscriptionCurrentPeriodStart` | date |  |
| `data[].subscriptionDurationType` | string |  |
| `data[].subscriptionId` | number |  |
| `data[].subscriptionIsCancelled` | boolean |  |
| `data[].subscriptionIsCancelledAtPeriodEnd` | boolean |  |
| `data[].subscriptionMessage` | string |  |
| `data[].subscriptionUpdatedOn` | date |  |
| `data[].transactionId` | string |  |
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

Through the native Buy Me a Coffee API, this operation is `GET /subscriptions` (base URL `https://developers.buymeacoffee.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

