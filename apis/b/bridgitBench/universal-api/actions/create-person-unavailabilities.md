# Bridgit Bench: Create Person Unavailabilities



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-unavailabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-unavailabilities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "id": 1,
  "payload[]": [
    {}
  ],
  "payload[].startDate": "2026-05-07T12:00:00.000Z",
  "payload[].isPrivate": true,
  "payload[].rangeType": "PostEmployment"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-unavailabilities', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "id": 1,
    "payload[]": [{}],
    "payload[].startDate": "2026-05-07T12:00:00.000Z",
    "payload[].isPrivate": true,
    "payload[].rangeType": "PostEmployment"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `id` | number | yes | Id of the person to get unavailabilities for |
| `payload[]` | array<object> | yes |  |
| `payload[].description` | string | no |  |
| `payload[].startDate` | date | yes |  |
| `payload[].endDate` | date | no |  |
| `payload[].isPrivate` | boolean | yes |  |
| `payload[].rangeType` | list<string> | yes | One of: `PostEmployment`, `PreEmployment`, `TimeOff`, `Unavailability`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/persons/:id/unavailabilities` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-unavailabilities.md) for the provider-specific parameters and requirements.

