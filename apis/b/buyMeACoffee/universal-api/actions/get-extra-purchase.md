# Buy Me a Coffee: Get Extra Purchase

Retrieves an extra purchase from Buy Me a Coffee by purchase ID.

```
GET https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-extra-purchase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buy Me a Coffee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-extra-purchase?connectionId=$CONNECTION_ID&id=2621" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2621"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buyMeACoffee/latest/actions/get-extra-purchase?${params}`, {
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
| `id` | number | yes | The unique ID of the extra purchase returned by the list extras purchases action. Example: `2621`. |

## Response

```json
{
  "success": true,
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
      "purchaseUpdatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `extra` | object |  |
| `extra.rewardCoffeePrice` | string |  |
| `extra.rewardConfirmationMessage` | string |  |
| `extra.rewardCreatedOn` | date |  |
| `extra.rewardDeletedOn` | date |  |
| `extra.rewardDescription` | string |  |
| `extra.rewardId` | number |  |
| `extra.rewardImage` | string |  |
| `extra.rewardIsActive` | number |  |
| `extra.rewardOrder` | number |  |
| `extra.rewardQuestion` | string |  |
| `extra.rewardSlots` | number |  |
| `extra.rewardTitle` | string |  |
| `extra.rewardUpdatedOn` | date |  |
| `extra.rewardUsed` | number |  |
| `payerEmail` | string |  |
| `payerName` | string |  |
| `purchaseAmount` | string |  |
| `purchaseCurrency` | string |  |
| `purchasedOn` | date |  |
| `purchaseId` | number |  |
| `purchaseIsRevoked` | number |  |
| `purchaseQuestion` | string |  |
| `purchaseUpdatedOn` | date |  |

## Native endpoint

Through the native Buy Me a Coffee API, this operation is `GET /extras/:id` (base URL `https://developers.buymeacoffee.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-extra-purchase.md) for the provider-specific parameters and requirements.

