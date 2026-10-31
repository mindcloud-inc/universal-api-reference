# Bridgit Bench: Update Person Title



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-person-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-person-title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "personId": 1,
  "entryId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/update-person-title', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "personId": 1,
    "entryId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `personId` | number | yes | Id of the person the entry belongs to |
| `entryId` | number | yes | Id of the title entry to update |
| `payload` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/titles/:entryId` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-person-title.md) for the provider-specific parameters and requirements.

