# Zoho Sprints: List Projects

Retrieves projects from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-projects?connectionId=$CONNECTION_ID&teamId=string&index=1&range=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "index": "1",
  "range": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-projects?${params}`, {
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
| `teamId` | string | yes |  |
| `index` | number | yes |  |
| `range` | number | yes |  |
| `projectstatus` | number | no |  |
| `viewby` | number | no |  |
| `searchvalue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": true,
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
| `next` | boolean |  |
| `project_prop` | object |  |
| `projectIds` | array<string> |  |
| `projectJObj` | object |  |
| `status` | string |  |
| `userDisplayName` | object |  |
| `zsuserIdvsZUID` | object |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/projects/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

