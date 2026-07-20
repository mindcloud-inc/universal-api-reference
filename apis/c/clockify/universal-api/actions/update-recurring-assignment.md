# Clockify: Update Recurring Assignment

Updates a recurring assignment in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-recurring-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-recurring-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assignmentId": "string",
  "end": "string",
  "start": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-recurring-assignment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assignmentId": "string",
    "end": "string",
    "start": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignmentId` | string | yes |  |
| `billable` | boolean | no |  |
| `end` | string | yes |  |
| `hoursPerDay` | number | no |  |
| `includeNonWorkingDays` | boolean | no |  |
| `note` | string | no |  |
| `seriesUpdateOption` | list | no | One of: `ALL`, `THIS_AND_FOLLOWING`, `THIS_ONE`. |
| `start` | string | yes |  |
| `startTime` | string | no |  |
| `taskId` | string | no |  |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].billable` | boolean |  |
| `items[].excludeDays[]` | array<object> |  |
| `items[].excludeDays[].date` | date |  |
| `items[].excludeDays[].type` | string |  |
| `items[].hoursPerDay` | number |  |
| `items[].id` | string |  |
| `items[].includeNonWorkingDays` | boolean |  |
| `items[].note` | string |  |
| `items[].period` | object |  |
| `items[].period.end` | date |  |
| `items[].period.start` | date |  |
| `items[].projectId` | string |  |
| `items[].published` | boolean |  |
| `items[].recurring` | object |  |
| `items[].recurring.repeat` | boolean |  |
| `items[].recurring.seriesId` | string |  |
| `items[].recurring.weeks` | number |  |
| `items[].startTime` | string |  |
| `items[].userId` | string |  |
| `items[].workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PATCH workspaces/:workspaceId/scheduling/assignments/recurring/:assignmentId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recurring-assignment.md) for the provider-specific parameters and requirements.

