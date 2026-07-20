# Zoho Sprints: Complete Sprint

Completes an existing sprint in Zoho Sprints.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/complete-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/complete-sprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string",
  "sprintId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/complete-sprint', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string",
    "sprintId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes |  |
| `projectId` | string | yes |  |
| `sprintId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDate": "2026-05-07T12:00:00.000Z",
      "sprintNo": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDate` | date |  |
| `sprintNo` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `POST /team/:teamId/projects/:projectId/sprints/:sprintId/complete/?action=complete` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-sprint.md) for the provider-specific parameters and requirements.

