# Billwerkplus: Put Subscription On Hold

Puts a subscription on hold in Billwerkplus.

```
PUT https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/put-subscription-on-hold
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/put-subscription-on-hold" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/put-subscription-on-hold', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Subscription handle. |
| `compensationMethod` | string | no | Compensation method for the current partial period. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /subscription/:handle/on_hold` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-subscription-on-hold.md) for the provider-specific parameters and requirements.

