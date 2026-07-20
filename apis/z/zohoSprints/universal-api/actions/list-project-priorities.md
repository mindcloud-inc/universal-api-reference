# Zoho Sprints: List Project Priorities

Retrieves project priorities from Zoho Sprints.

```
GET https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-project-priorities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sprints `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-project-priorities?connectionId=$CONNECTION_ID&teamId=string&projectId=string&index=1&range=10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "projectId": "string",
  "index": "1",
  "range": "10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSprints/latest/actions/list-project-priorities?${params}`, {
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
| `index` | number | yes | Default: `1`. |
| `range` | number | yes | Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "maxPrioCount": 1,
      "next": true,
      "projPriority_prop": {},
      "projPriorityIds": [
        "string"
      ],
      "projPriorityJObj": {},
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
| `maxPrioCount` | number |  |
| `next` | boolean |  |
| `projPriority_prop` | object |  |
| `projPriorityIds` | array<string> |  |
| `projPriorityJObj` | object |  |
| `status` | string |  |
| `userDisplayName` | object |  |
| `zsuserIdvsZUID` | object |  |

## Native endpoint

Through the native Zoho Sprints API, this operation is `GET /team/:teamId/projects/:projectId/priority/` (base URL `https://sprintsapi.zoho.com/zsapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-priorities.md) for the provider-specific parameters and requirements.

