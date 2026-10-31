# Bridgit Bench: Create Person



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "name": "Ava Chen",
  "type": "Hourly",
  "workDays": [
    1,
    2,
    3,
    4,
    5
  ],
  "fields[].fieldId": 1,
  "fields[].values[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "name": "Ava Chen",
    "type": "Hourly",
    "workDays": [1,2,3,4,5],
    "fields[].fieldId": 1,
    "fields[].values[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `email` | string | no |  |
| `uniqueId` | string | no |  |
| `name` | string | yes |  |
| `type` | list<string> | yes | One of: `Hourly`, `Salaried`. |
| `title` | string | no |  |
| `photoUrl` | string | no |  |
| `employmentDates` | object | no | Request object for representing employment dates on a person. |
| `workDays` | list<number> | yes | One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Accepts multiple values as an array. Default: `[1,2,3,4,5]`. |
| `fields[]` | array<object> | no |  |
| `fields[].fieldId` | number | yes |  |
| `fields[].values[]` | array<string> | yes |  |
| `groupings[]` | array<number> | no |  |
| `industryStartDate` | date | no |  |
| `titleEffectiveDate` | date | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/Persons` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

