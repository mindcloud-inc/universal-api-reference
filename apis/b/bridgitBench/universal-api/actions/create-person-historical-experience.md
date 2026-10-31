# Bridgit Bench: Create Person Historical Experience



```
POST https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-historical-experience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bridgit Bench `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-historical-experience" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "personId": 1,
  "projectName": "Ava Chen",
  "roleName": "Ava Chen",
  "currentCompany": true,
  "experienceFields[]": [
    {}
  ],
  "experienceFields[].experienceFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-person-historical-experience', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "personId": 1,
    "projectName": "Ava Chen",
    "roleName": "Ava Chen",
    "currentCompany": true,
    "experienceFields[]": [{}],
    "experienceFields[].experienceFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | The account ID. |
| `personId` | number | yes | The person ID. |
| `projectName` | string | yes |  |
| `projectStartDate` | date | no |  |
| `projectEndDate` | date | no |  |
| `roleName` | string | yes |  |
| `currentCompany` | boolean | yes |  |
| `experienceFields[]` | array<object> | yes |  |
| `experienceFields[].experienceFieldId` | string | yes |  |
| `experienceFields[].experienceFieldValueId` | string | no |  |
| `experienceFields[].value` | string | no |  |
| `projectDescription` | string | no |  |
| `companyName` | string | no |  |
| `assignmentStartDate` | date | no |  |
| `assignmentEndDate` | date | no |  |
| `assignmentDuration` | number | no |  |
| `assignmentHours` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bridgit Bench API returns.

## Native endpoint

Through the native Bridgit Bench API, this operation is `POST /rp/api/v1/accounts/:accountId/persons/:personId/historical-experiences` (base URL `https://bench.gobridgit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-historical-experience.md) for the provider-specific parameters and requirements.

