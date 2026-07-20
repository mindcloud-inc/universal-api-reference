# Float: Create Phase

Creates a new phase in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-phase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-phase" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endDate": "2026-03-18",
  "name": "Discovery",
  "projectId": "11207922",
  "startDate": "2026-03-17"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-phase', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endDate": "2026-03-18",
    "name": "Discovery",
    "projectId": "11207922",
    "startDate": "2026-03-17"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | yes | The end date of this phase Example: `2026-03-18`. |
| `name` | string | yes | The name of the phase Example: `Discovery`. |
| `projectId` | number | yes | The ID of the project to which this phase belongs Example: `11207922`. |
| `startDate` | string | yes | The start date of this phase Example: `2026-03-17`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "budgetTotal": {},
      "color": {},
      "created": "string",
      "defaultHourlyRate": {},
      "endDate": "string",
      "modified": "string",
      "name": "Ava Chen",
      "nonBillable": {},
      "notes": {},
      "phaseId": 1,
      "projectId": 1,
      "startDate": "string",
      "status": 1,
      "tentative": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `budgetTotal` | object |  |
| `color` | object |  |
| `created` | string |  |
| `defaultHourlyRate` | object |  |
| `endDate` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `nonBillable` | object |  |
| `notes` | object |  |
| `phaseId` | number |  |
| `projectId` | number |  |
| `startDate` | string |  |
| `status` | number |  |
| `tentative` | number |  |

## Native endpoint

Through the native Float API, this operation is `POST /phases` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-phase.md) for the provider-specific parameters and requirements.

