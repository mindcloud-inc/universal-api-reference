# Zoho Sprints: List Sprints

Retrieves sprints from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-sprints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-sprints?connectionId=$CONNECTION_ID&teamId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-sprints?${params}`, {
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
| `sprintTypeArr` | string | no |  |
| `searchValue` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next": true,
      "sprint_prop": {},
      "sprintIds": [
        "string"
      ],
      "sprintJObj": {},
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
| `sprint_prop` | object |  |
| `sprintIds` | array<string> |  |
| `sprintJObj` | object |  |
| `status` | string |  |
| `userDisplayName` | object |  |
| `zsuserIdvsZUID` | object |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/projects/:projectId/sprints/?action=data&index=1&range=50&type={{sprintTypeArr}}&searchvalue={{searchValue}}` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sprints.md) for the provider-specific parameters and requirements.

