# Bridgit Bench: Update Account Phases



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-account-phases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-account-phases" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "payload[]": [
    {}
  ],
  "payload[].id": 1,
  "payload[].name": "Ava Chen",
  "payload[].includeOnNewProjects": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-account-phases', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "payload[]": [{}],
    "payload[].id": 1,
    "payload[].name": "Ava Chen",
    "payload[].includeOnNewProjects": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `payload[]` | array<object> | yes |  |
| `payload[].id` | number | yes |  |
| `payload[].name` | string | yes |  |
| `payload[].includeOnNewProjects` | boolean | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PUT /rp/api/v1/accounts/:accountId/Phases` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account-phases.md) for the provider-specific parameters and requirements.

