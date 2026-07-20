# SureCart: Retrieve Price



```
GET https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-price?connectionId=$CONNECTION_ID&id=08f7b8e3-7114-4a9b-b40e-f6fdf52a4fb4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "08f7b8e3-7114-4a9b-b40e-f6fdf52a4fb4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/retrieve-price?${params}`, {
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
| `id` | string | yes | The price ID to retrieve. Example: `08f7b8e3-7114-4a9b-b40e-f6fdf52a4fb4`. |

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

Through the native SureCart API, this operation is `GET v1/prices/:id` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-price.md) for the provider-specific parameters and requirements.

