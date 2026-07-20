# Clockify: Update Balance

Updates a time off balance in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-balance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "policyId": "string",
  "userIds[]": [
    "string"
  ],
  "value": "100"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-balance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "policyId": "string",
    "userIds[]": ["string"],
    "value": "100"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `policyId` | string<string> | yes |  |
| `userIds[]` | array<string> | yes |  |
| `value` | number | yes | Example: `100`. |
| `note` | string | no | Example: `Sample note`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balances": [
        [
          {}
        ]
      ],
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balances[]` | array<object> |  |
| `balances[].balance` | number |  |
| `balances[].id` | string |  |
| `balances[].negativeBalanceAmount` | number |  |
| `balances[].negativeBalanceLimit` | boolean |  |
| `balances[].policyArchived` | boolean |  |
| `balances[].policyId` | string |  |
| `balances[].policyName` | string |  |
| `balances[].policyTimeUnit` | string |  |
| `balances[].total` | number |  |
| `balances[].used` | number |  |
| `balances[].userId` | string |  |
| `balances[].userName` | string |  |
| `balances[].workspaceId` | string |  |
| `count` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/time-off/balance/policy/:policyId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-balance.md) for the provider-specific parameters and requirements.

