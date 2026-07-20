# Zoho Sprints: Get Project Details

Retrieves project details from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-project-details?connectionId=$CONNECTION_ID&teamId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/get-project-details?${params}`, {
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
| `projectId` | string | yes |  |

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

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/projects/:projectId/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-details.md) for the provider-specific parameters and requirements.

