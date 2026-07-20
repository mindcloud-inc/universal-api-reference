# Cratejoy: Get Subscription

Retrieves a subscription from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-subscription?connectionId=$CONNECTION_ID&subscriptionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriptionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/get-subscription?${params}`, {
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
| `subscriptionId` | number | yes | The Cratejoy subscription ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autorenew": true,
      "credit": 1,
      "end_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "product_billing_id": 1,
      "skipped_date": "2026-05-07T12:00:00.000Z",
      "start_date": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autorenew` | boolean |  |
| `credit` | number |  |
| `end_date` | date |  |
| `id` | number |  |
| `note` | string |  |
| `product_billing_id` | number |  |
| `skipped_date` | date |  |
| `start_date` | date |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `GET /v1/subscriptions/:subscriptionId/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

