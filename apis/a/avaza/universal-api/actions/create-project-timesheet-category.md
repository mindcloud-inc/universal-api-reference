# Avaza: Create Project Timesheet Category

Creates a new project timesheet category in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project-timesheet-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project-timesheet-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-project-timesheet-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectidfk` | number | no |  |
| `timesheetcategoryidfk` | number | no |  |
| `isbillable` | boolean | no |  |
| `ispayable` | boolean | no |  |
| `rateamount` | number | no |  |
| `budgethours` | number | no |  |
| `costamount` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/ProjectTimesheetCategory` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-timesheet-category.md) for the provider-specific parameters and requirements.

