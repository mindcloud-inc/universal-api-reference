# Float: Create Allocation

Creates a new allocation in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "startDate": "string",
  "endDate": "string",
  "hours": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-allocation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "startDate": "string",
    "endDate": "string",
    "hours": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The ID of the project for this allocation |
| `phaseId` | number | no | The ID of the project phase for this allocation |
| `startDate` | string | yes | Start date of this allocation |
| `endDate` | string | yes | End date of this allocation |
| `startTime` | string | no | Start time in 24 hour format |
| `hours` | number | yes | Number of hours per day |
| `peopleId` | number | no | The ID of the person assigned to the allocation |
| `peopleIds` | list<number> | no | List of one or more people IDs assigned to the allocation |
| `status` | number | no | Status of the allocation |
| `name` | string | no | Name of the associated project task |
| `taskMetaId` | number | no | The ID of the associated project task |
| `notes` | string | no | Additional details about the work required |
| `repeatState` | number | no | Frequency that this allocation repeats |
| `repeatEndDate` | string | no | Date that the repeating allocation will cease |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": 1,
      "created": "string",
      "createdBy": 1,
      "endDate": "string",
      "hours": 1,
      "modified": "string",
      "modifiedBy": 1,
      "name": "Ava Chen",
      "notes": {},
      "parentTaskId": {},
      "peopleId": 1,
      "phaseId": 1,
      "projectId": 1,
      "repeatEndDate": {},
      "repeatState": 1,
      "rootTaskId": {},
      "startDate": "string",
      "startTime": {},
      "status": 1,
      "taskId": 1,
      "taskMetaId": 1
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
| `endDate` | string |  |
| `hours` | number |  |
| `modified` | string |  |
| `modifiedBy` | number |  |
| `name` | string |  |
| `notes` | object |  |
| `parentTaskId` | object |  |
| `peopleId` | number |  |
| `phaseId` | number |  |
| `projectId` | number |  |
| `repeatEndDate` | object |  |
| `repeatState` | number |  |
| `rootTaskId` | object |  |
| `startDate` | string |  |
| `startTime` | object |  |
| `status` | number |  |
| `taskId` | number |  |
| `taskMetaId` | number |  |

## Native endpoint

Through the native Float API, this operation is `POST /tasks` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-allocation.md) for the provider-specific parameters and requirements.

