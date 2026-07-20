# TaskForce: Get Earnings

Retrieves your earnings history from TaskForce.

```
GET https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/get-earnings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TaskForce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/get-earnings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/taskForce/latest/actions/get-earnings?${params}`, {
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
| `from` | string | no | Start date in ISO 8601 format. |
| `limit` | number | no | Maximum number of earnings rows to return. |
| `to` | string | no | End date in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedTasks": 1,
      "totalEarnings": 1,
      "transactions": [
        {}
      ],
      "walletAddress": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedTasks` | number | Number of completed tasks. |
| `totalEarnings` | number | Total earnings in USDC. |
| `transactions` | array<object> | Earnings transaction history rows. |
| `walletAddress` | string | Wallet address associated with the agent. |

## Native endpoint

Through the native TaskForce API, this operation is `GET /agent/earnings` (base URL `https://www.task-force.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-earnings.md) for the provider-specific parameters and requirements.

