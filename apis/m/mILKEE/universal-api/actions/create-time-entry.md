# MILKEE: Create Time Entry

Creates a new time entry in MILKEE.

```
POST https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "4640",
  "date": "string",
  "hours": 1,
  "minutes": 1,
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "4640",
    "date": "string",
    "hours": 1,
    "minutes": 1,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billable` | boolean | no | Whether the time is billable. |
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |
| `date` | string | yes | Date of work. |
| `description` | string | no | Description of work performed. |
| `end` | string | no | End time in H:i format. |
| `hourlyRate` | number | no | Hourly rate for the entry. |
| `hours` | number | yes | Hours worked. |
| `minutes` | number | yes | Minutes worked. |
| `projectId` | number | yes | ID of the project. |
| `start` | string | no | Start time in H:i format. |
| `taskId` | number | no | Associated task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native MILKEE API, this operation is `POST /companies/:companyId/times` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.

