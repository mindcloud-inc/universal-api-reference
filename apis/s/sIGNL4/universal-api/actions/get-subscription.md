# SIGNL4: Get Subscription

Retrieves a subscription from SIGNL4 by ID.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-subscription?connectionId=$CONNECTION_ID&subscriptionId=sample-subscription-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "sample-subscription-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-subscription?${params}`, {
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
| `subscriptionId` | string | yes | SIGNL4 subscription ID. Example: `sample-subscription-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "elmEnabled": true,
      "externalAccountId": "string",
      "id": "string",
      "isBetaMember": true,
      "name": "Ava Chen",
      "nextBilling": "2026-05-07T12:00:00.000Z",
      "ownerId": "string",
      "planCode": "string",
      "planState": 1,
      "referralEnabled": true,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `currency` | string |  |
| `elmEnabled` | boolean |  |
| `externalAccountId` | string |  |
| `id` | string |  |
| `isBetaMember` | boolean |  |
| `name` | string |  |
| `nextBilling` | date |  |
| `ownerId` | string |  |
| `planCode` | string |  |
| `planState` | number |  |
| `referralEnabled` | boolean |  |
| `status` | number |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/subscriptions/{subscriptionId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

