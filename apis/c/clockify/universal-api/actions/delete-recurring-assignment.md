# Clockify: Delete Recurring Assignment

Deletes a recurring assignment from Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-recurring-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-recurring-assignment?connectionId=$CONNECTION_ID&assignmentId=string&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assignmentId": "string",
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/delete-recurring-assignment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignmentId` | string | yes |  |
| `seriesUpdateOption` | list | no | One of: `ALL`, `THIS_AND_FOLLOWING`, `THIS_ONE`. |
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

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/scheduling/assignments/recurring/:assignmentId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-recurring-assignment.md) for the provider-specific parameters and requirements.

