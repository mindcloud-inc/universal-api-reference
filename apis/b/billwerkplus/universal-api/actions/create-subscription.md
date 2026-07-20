# Billwerkplus: Create Subscription

Creates a subscription in Billwerkplus.

```
POST https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": "string",
  "plan": "string",
  "handle": "string",
  "signupMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": "string",
    "plan": "string",
    "handle": "string",
    "signupMethod": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | string | yes | Existing customer handle. |
| `plan` | string | yes | Plan handle. |
| `handle` | string | yes | Unique subscription handle. |
| `signupMethod` | string | yes | How the customer provides payment information. |
| `test` | boolean | no | Create the subscription in test mode. Default: `true`. |
| `showTerms` | boolean | no | Show terms of service on the signup page. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | string | no | Future start date for the subscription. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /subscription` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-subscription.md) for the provider-specific parameters and requirements.

