# SureCart: Create Refund



```
POST https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureCart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refund.amount": "500",
  "refund.reason": "requested_by_customer",
  "refund.chargeId": "5c8123b5-7346-494f-a644-f15b1d2cbf25"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureCart/latest/actions/create-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refund.amount": "500",
    "refund.reason": "requested_by_customer",
    "refund.chargeId": "5c8123b5-7346-494f-a644-f15b1d2cbf25"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refund.amount` | number | yes | Refund amount in cents. Example: `500`. |
| `refund.reason` | string | yes | Refund reason, for example requested_by_customer. Example: `requested_by_customer`. |
| `refund.chargeId` | string | yes | The charge ID to refund. Example: `5c8123b5-7346-494f-a644-f15b1d2cbf25`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SureCart API returns.

## Native endpoint

Through the native SureCart API, this operation is `POST v1/refunds` (base URL `https://api.surecart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refund.md) for the provider-specific parameters and requirements.

