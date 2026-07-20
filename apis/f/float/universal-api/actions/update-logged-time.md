# Float: Update Logged Time

Updates an existing logged time entry in Float.

```
PUT https://connect.mindcloud.co/v1/universal/float/latest/actions/update-logged-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/float/latest/actions/update-logged-time" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "loggedTimeId": "string",
  "peopleId": 1,
  "date": "string",
  "hours": 1,
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/update-logged-time', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "loggedTimeId": "string",
    "peopleId": 1,
    "date": "string",
    "hours": 1,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `loggedTimeId` | string | yes | Unique ID of the specific logged time entry to be updated |
| `peopleId` | number | yes | The ID of the person for the logged time entry |
| `date` | string | yes | Date of the logged time entry |
| `referenceDate` | string | no | The date on which to suppress a matching logged time suggestion |
| `hours` | number | yes | Total hours of the logged time entry |
| `notes` | string | no | Additional notes about this logged time entry |
| `projectId` | number | yes | The ID of the project on which this entry was logged |
| `phaseId` | number | no | The ID of the project phase for which this entry was logged |
| `taskId` | number | no | The ID of a scheduled allocation linked to this entry |
| `taskName` | string | no | The name of the project task against which this entry was logged |
| `taskMetaId` | number | no | The ID of the associated project task |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": 1,
      "created": "string",
      "createdBy": 1,
      "date": "string",
      "hours": 1,
      "locked": 1,
      "lockedDate": {},
      "loggedTimeId": "string",
      "modified": "string",
      "modifiedBy": 1,
      "notes": "string",
      "peopleId": 1,
      "phaseId": 1,
      "priority": 1,
      "projectId": 1,
      "referenceDate": {},
      "taskId": 1,
      "taskMetaId": 1,
      "taskName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | number |  |
| `created` | string |  |
| `createdBy` | number |  |
| `date` | string |  |
| `hours` | number |  |
| `locked` | number |  |
| `lockedDate` | object |  |
| `loggedTimeId` | string |  |
| `modified` | string |  |
| `modifiedBy` | number |  |
| `notes` | string |  |
| `peopleId` | number |  |
| `phaseId` | number |  |
| `priority` | number |  |
| `projectId` | number |  |
| `referenceDate` | object |  |
| `taskId` | number |  |
| `taskMetaId` | number |  |
| `taskName` | string |  |

## Native endpoint

Through the native Float API, this operation is `PATCH /logged-time/:logged_time_id` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-logged-time.md) for the provider-specific parameters and requirements.

