# Clockify: Get User Balance

Retrieves a user's time off balance from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-user-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-user-balance?connectionId=$CONNECTION_ID&workspaceId=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-user-balance?${params}`, {
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
| `userId` | string<string> | yes |  |

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

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/time-off/balance/user/:userId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-balance.md) for the provider-specific parameters and requirements.

