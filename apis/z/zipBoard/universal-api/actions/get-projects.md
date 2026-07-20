# zipBoard: Get Projects

Retrieves projects from zipBoard.

```
GET https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-projects?connectionId=$CONNECTION_ID&orgId=string&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "string",
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-projects?${params}`, {
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
| `orgId` | string | yes | Organization ID to fetch projects for. |
| `orgId` | string | yes |  |
| `owner` | boolean | no | Return projects where the authenticated user is the owner. |
| `projectId` | string | no | Optional project ID filter. |
| `role` | string | no | Optional role filter: owner, manager, or reviewer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "Id": "string",
      "isEnabled": true,
      "orgId": "string",
      "projectId": "string",
      "screenCount": 1,
      "taskCount": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `Id` | string |  |
| `isEnabled` | boolean |  |
| `orgId` | string |  |
| `projectId` | string |  |
| `screenCount` | number |  |
| `taskCount` | number |  |
| `title` | string |  |

## Native endpoint

Through the native zipBoard API, this operation is `GET /projects` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-projects.md) for the provider-specific parameters and requirements.

