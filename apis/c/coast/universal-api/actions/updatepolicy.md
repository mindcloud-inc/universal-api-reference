# Coast: Update Policy By ID



```
PUT https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatepolicy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatepolicy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "string",
  "type": "string",
  "name": "Ava Chen",
  "archived": true,
  "timezone": "string",
  "customSpendControls[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatepolicy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": "string",
    "type": "string",
    "name": "Ava Chen",
    "archived": true,
    "timezone": "string",
    "customSpendControls[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | string | yes | Coast policy ID of the policy to update. |
| `type` | string | yes | Updated type for the policy. |
| `name` | string | yes | Updated name for the policy. |
| `archived` | boolean | yes | Whether the policy should be archived. |
| `timezone` | string | yes | Updated timezone for the policy. |
| `customSpendControls[]` | array<object> | yes | Updated custom spend controls for the policy. |
| `allowedPurchaseTimeWindows` | string | no | Updated allowed purchase time windows for the policy. |
| `globalSpendLimits` | object | no | Updated global spend limits for the policy. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `PUT /v2/policies/:policyId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/updatepolicy.md) for the provider-specific parameters and requirements.

