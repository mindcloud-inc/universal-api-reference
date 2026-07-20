# SureCart: List Prices



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-prices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/list-prices?${params}`, {
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
| `adHoc` | boolean | no | Only return prices that allow ad hoc amounts or not. |
| `archived` | boolean | no | Only return archived or active prices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adHoc": true,
      "adHocMaxAmount": 1,
      "adHocMinAmount": 1,
      "amount": 1,
      "archived": true,
      "createdAt": 1,
      "currency": "string",
      "currentVersion": true,
      "fullAmount": 1,
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "portalSubscriptionUpdateEnabled": true,
      "position": 1,
      "product": "string",
      "recurringEndBehavior": "string",
      "recurringInterval": "string",
      "recurringIntervalCount": 1,
      "recurringPeriodCount": 1,
      "renewalPrice": "string",
      "restartSubscriptionOnCompleted": true,
      "revokeAfterDays": 1,
      "revokePurchasesOnCompleted": true,
      "scratchAmount": 1,
      "setupFeeAmount": 1,
      "setupFeeEnabled": true,
      "setupFeeName": "Ava Chen",
      "setupFeeTrialEnabled": true,
      "trialDurationDays": 1,
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adHoc` | boolean |  |
| `adHocMaxAmount` | number |  |
| `adHocMinAmount` | number |  |
| `amount` | number |  |
| `archived` | boolean |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `currentVersion` | boolean |  |
| `fullAmount` | number |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `portalSubscriptionUpdateEnabled` | boolean |  |
| `position` | number |  |
| `product` | string |  |
| `recurringEndBehavior` | string |  |
| `recurringInterval` | string |  |
| `recurringIntervalCount` | number |  |
| `recurringPeriodCount` | number |  |
| `renewalPrice` | string |  |
| `restartSubscriptionOnCompleted` | boolean |  |
| `revokeAfterDays` | number |  |
| `revokePurchasesOnCompleted` | boolean |  |
| `scratchAmount` | number |  |
| `setupFeeAmount` | number |  |
| `setupFeeEnabled` | boolean |  |
| `setupFeeName` | string |  |
| `setupFeeTrialEnabled` | boolean |  |
| `trialDurationDays` | number |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native SureCart API, this operation is `GET v1/prices` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prices.md) for the provider-specific parameters and requirements.

