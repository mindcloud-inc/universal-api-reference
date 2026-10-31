# Bridgit Bench: Patch Person Historical Experience



```
PUT https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/patch-person-historical-experience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/patch-person-historical-experience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "personId": 1,
  "historicalExperienceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/patch-person-historical-experience', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "personId": 1,
    "historicalExperienceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `personId` | number | yes | The Person ID |
| `historicalExperienceId` | string | yes | The Historical Experience ID |
| `roleName` | string | no |  |
| `assignmentStartDate` | date | no |  |
| `assignmentEndDate` | date | no |  |
| `assignmentDuration` | number | no |  |
| `assignmentHours` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `PATCH /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences/:historicalExperienceId` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-person-historical-experience.md) for the provider-specific parameters and requirements.

