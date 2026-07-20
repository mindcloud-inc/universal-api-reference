# Clockify: Get Policy Balances

Retrieves time off policy balances from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-policy-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-policy-balances?connectionId=$CONNECTION_ID&workspaceId=string&policyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "policyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-policy-balances?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `policyId` | string<string> | yes |  |

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

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/time-off/balance/policy/:policyId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-policy-balances.md) for the provider-specific parameters and requirements.

