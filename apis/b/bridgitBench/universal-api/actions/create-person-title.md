# Bridgit Bench: Create Person Title



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-title" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "personId": 1,
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-title', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "personId": 1,
    "startDate": "2026-05-07T12:00:00.000Z",
    "endDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `personId` | number | yes | Id of the person to add the entry to |
| `titleValueId` | number | no | The account title list value to record; mutually exclusive with `title`. |
| `title` | string | no | A freeform title; mutually exclusive with `titleValueId`. |
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/persons/:personId/titles` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-title.md) for the provider-specific parameters and requirements.

