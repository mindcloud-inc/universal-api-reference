# Bridgit Bench: Set Role Names



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-role-names
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-role-names" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "payload[]": [
    {}
  ],
  "payload[].id": 1,
  "payload[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/set-role-names', {
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
    "payload[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The account ID |
| `alphabetize` | boolean | no | Optional flag to set whether role names should be alphabetically ordered by the caller Default: `false`. |
| `payload[]` | array<object> | yes |  |
| `payload[].id` | number | yes |  |
| `payload[].name` | string | yes |  |
| `payload[].cost` | number | no |  |
| `payload[].isHidden` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/role-names` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-role-names.md) for the provider-specific parameters and requirements.

