# Zoho Sprints: Create Sprint

Creates a new sprint in Zoho Sprints.

```
POST https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/create-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/create-sprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string",
  "sprintName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/create-sprint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string",
    "sprintName": "Ava Chen"
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
| `sprintName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permission_prop": {},
      "permissionJObj": {},
      "sprintId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permission_prop` | object |  |
| `permissionJObj` | object |  |
| `sprintId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `POST /team/:teamId/projects/:projectId/sprints/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sprint.md) for the provider-specific parameters and requirements.

