# Zoho Sprints: Update Project

Updates an existing project in Zoho Sprints.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string"
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
| `name` | string | no |  |
| `status` | string | no |  |
| `projgroup` | string | no |  |
| `owner` | string | no |  |
| `startdate` | string | no |  |
| `enddate` | string | no |  |
| `projectlayoutid` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isStrictScrum": true,
      "prefix": "string",
      "project_prop": {},
      "projectIds": [
        "string"
      ],
      "projectJObj": {},
      "status": "string",
      "userDisplayName": {},
      "zsuserIdvsZUID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isStrictScrum` | boolean |  |
| `prefix` | string |  |
| `project_prop` | object |  |
| `projectIds` | array<string> |  |
| `projectJObj` | object |  |
| `status` | string |  |
| `userDisplayName` | object |  |
| `zsuserIdvsZUID` | object |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `POST /team/:teamId/projects/:projectId/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

