# Rocketlane: Search Time Entries

Searches time entries in Rocketlane.

```
GET https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/search-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/search-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/search-time-entries?${params}`, {
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
| `includeFields` | string | no | This query parameter allows you to specify which fields should be returned in the response body by selecting from the drop down. To get the relevant fields, use comma separated values. If the field is left blank, the default properties are returned. |
| `includeAllFields` | boolean | no | This query parameter allows you to specify if all the fields should be returned in the response body. If the field is left blank, the default properties are returned. |
| `match` | string | no | You can use the match param to specify if we need to filter the entries using either AND(all) / OR(any). Defaults to AND. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityName": "Ava Chen",
      "approvedAt": 1,
      "approvedBy": {},
      "billable": true,
      "billRate": {},
      "category": {},
      "costRate": {},
      "createdAt": 1,
      "createdBy": {},
      "date": "string",
      "deleted": true,
      "fields": [
        {}
      ],
      "minutes": 1,
      "notes": "string",
      "project": {},
      "projectPhase": {},
      "rejectedAt": 1,
      "rejectedBy": {},
      "sourceType": "string",
      "status": "string",
      "submittedAt": 1,
      "submittedBy": {},
      "task": {},
      "timeEntryId": 1,
      "updatedAt": 1,
      "updatedBy": {},
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityName` | string | Name of the adhoc activity being performed |
| `approvedAt` | number | Time of approval for time entry |
| `approvedBy` | object | User who approved the time entry |
| `billable` | boolean | Whether the time entry is billable. Defaults to true |
| `billRate` | object | The hourly rate charged to customers for the projects or services provided. |
| `category` | object | Category associated with the time entry |
| `costRate` | object | The hourly rate assigned to employees for the work they perform for your organization |
| `createdAt` | number | Timestamp of creation time of the entry in epoch milliseconds |
| `createdBy` | object | The team member who created the time entry. |
| `date` | string | Date of the time entry in format YYYY-MM-DD |
| `deleted` | boolean | Whether the time entry is deleted. |
| `fields` | array<object> | Custom fields associated with the time entry |
| `minutes` | number | Duration of the time entry in minutes |
| `notes` | string | Notes for the time entry |
| `project` | object | Project associated with the time entry |
| `projectPhase` | object | Project phase associated with the time entry |
| `rejectedAt` | number | Time of rejection for time entry |
| `rejectedBy` | object | User who rejected the time entry |
| `sourceType` | string | Type of source of the time entry Eg: Task, Adhoc (Activity), Milestone |
| `status` | string | Status of the time entry |
| `submittedAt` | number | Time of submission for time entry  Note: This field may be null, even when the time entry is in an APPROVED or REJECTED state, as time entries can be approved or rejected without an explicit submission step. |
| `submittedBy` | object | User who submitted the time entry  Note: This field may be null, even when the time entry is in an APPROVED or REJECTED state, as time entries can be approved or rejected without an explicit submission step. |
| `task` | object | Task associated with the time entry |
| `timeEntryId` | number | The unique, system-generated identifier, which can be used to identify the time entry globally. |
| `updatedAt` | number | Timestamp of last updated time of the entry in epoch milliseconds |
| `updatedBy` | object | The team member who updated the ttime entry. |
| `user` | object | User associated with the time entry |

## Native endpoint

Through the native Rocketlane API, this operation is `GET /1.0/time-entries/search` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-time-entries.md) for the provider-specific parameters and requirements.

