# Float: List Allocations

Retrieves allocations from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-allocations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-allocations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-allocations?${params}`, {
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
| `projectId` | number | no | A project ID to filter the response on |
| `peopleId` | number | no | A people ID to filter the response on |
| `startDate` | string | no | Start of date range in format YYYY-MM-DD |
| `endDate` | string | no | End of date range in format YYYY-MM-DD |
| `status` | number | no | Filter response on the allocation status |
| `modifiedSince` | string | no | Filter on records with an equal or later modified timestamp |
| `fields` | string | no | Comma-delimited set of fields to include in the response |
| `expand` | string | no | Use task_days to return additional calculated dates for each allocation |

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
      "peopleIds": {},
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
| `peopleIds` | object |  |
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

Through the native Float API, this operation is `GET /tasks` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-allocations.md) for the provider-specific parameters and requirements.

