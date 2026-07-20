# Float: Create Milestone

Creates a new milestone in Float.

```
POST https://connect.mindcloud.co/v1/universal/float/latest/actions/create-milestone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/float/latest/actions/create-milestone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-03-18 09:00",
  "name": "Kickoff",
  "projectId": "11207922"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/float/latest/actions/create-milestone', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-03-18 09:00",
    "name": "Kickoff",
    "projectId": "11207922"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | Start date of the milestone Example: `2026-03-18 09:00`. |
| `name` | string | yes | The name of the milestone Example: `Kickoff`. |
| `phaseId` | number | no | The phase that this milestone belongs to Example: `2063834`. |
| `projectId` | number | yes | The project that this milestone belongs to Example: `11207922`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "date": "string",
      "endDate": "string",
      "milestoneId": 1,
      "modified": "string",
      "name": "Ava Chen",
      "phaseId": 1,
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `date` | string |  |
| `endDate` | string |  |
| `milestoneId` | number |  |
| `modified` | string |  |
| `name` | string |  |
| `phaseId` | number |  |
| `projectId` | number |  |

## Native endpoint

Through the native Float API, this operation is `POST /milestones` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-milestone.md) for the provider-specific parameters and requirements.

