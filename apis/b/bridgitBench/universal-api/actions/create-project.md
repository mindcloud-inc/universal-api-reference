# Bridgit Bench: Create Project



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "name": "Ava Chen",
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "type": "Awarded",
  "fields[].fieldId": 1,
  "fields[].values[]": [
    "string"
  ],
  "phases[].id": 1,
  "phases[].startDate": "2026-05-07T12:00:00.000Z",
  "phases[].endDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "name": "Ava Chen",
    "startDate": "2026-05-07T12:00:00.000Z",
    "endDate": "2026-05-07T12:00:00.000Z",
    "type": "Awarded",
    "fields[].fieldId": 1,
    "fields[].values[]": ["string"],
    "phases[].id": 1,
    "phases[].startDate": "2026-05-07T12:00:00.000Z",
    "phases[].endDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The Account ID |
| `name` | string | yes |  |
| `colour` | string | no | The color associated with the project, expressed as a web color string: a '#' character, followed by a six-digit hexadecimal number. If not provided, color rules will be evaluated. |
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |
| `startTime` | string | no | The daily start time for the project. When omitted, the account default is used, falling back to the rp-api default. |
| `endTime` | string | no | The daily end time for the project. When omitted, the account default is used, falling back to the rp-api default. |
| `workDays` | list<number> | no | The days of the week the project is active. When omitted, the account default is used, falling back to the rp-api default. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Accepts multiple values as an array. |
| `hoursPerWeek` | number | no | The number of hours per week a salaried person works, for forecasting and budgeting calculations. When omitted, the account default is used, falling back to the rp-api default. |
| `type` | list<string> | yes | One of: `Awarded`, `Opportunity`. |
| `winPercent` | number | no |  |
| `fields[]` | array<object> | no |  |
| `fields[].fieldId` | number | yes |  |
| `fields[].values[]` | array<string> | yes |  |
| `groupings[]` | array<number> | no |  |
| `description` | string | no |  |
| `phases[]` | array<object> | no |  |
| `phases[].id` | number | yes |  |
| `phases[].startDate` | date | yes |  |
| `phases[].endDate` | date | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/Projects` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

