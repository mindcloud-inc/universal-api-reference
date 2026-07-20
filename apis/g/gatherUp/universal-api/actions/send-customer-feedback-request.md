# GatherUp: Send Customer Feedback Request

Creates a customer feedback request in GatherUp.

```
POST https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/send-customer-feedback-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/send-customer-feedback-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/send-customer-feedback-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | number | yes | Customer id. |
| `ratingRevision` | number | no | 1 will send rating revision instead of new feedback request. 0 will create new feedback request. Default value is 1. |
| `checkThreshold` | number | no | 1 will check if threshold is reached If yes then it throws error. Default value is 0. |
| `jobId` | string | no | Sets JobID for repeat feedback request. Replaces existing JobID if rating revision. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /customer/feedback/send` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-customer-feedback-request.md) for the provider-specific parameters and requirements.

