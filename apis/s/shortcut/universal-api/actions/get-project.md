# Shortcut: Get Project



```
GET https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shortcut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-project?connectionId=$CONNECTION_ID&projectPublicId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectPublicId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shortcut/latest/actions/get-project?${params}`, {
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
| `projectPublicId` | number | yes | The public ID of the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abbreviation": "string",
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "entityType": "string",
      "id": 1,
      "name": "Ava Chen",
      "startTime": "2026-05-07T12:00:00.000Z",
      "teamId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string |  |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `description` | string |  |
| `entityType` | string |  |
| `id` | number |  |
| `name` | string |  |
| `startTime` | date |  |
| `teamId` | number |  |
| `updatedAt` | date |  |
| `workflowId` | number |  |

## Native endpoint

Through the native Shortcut API, this operation is `GET /projects/:projectPublicId` (base URL `https://api.app.shortcut.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

