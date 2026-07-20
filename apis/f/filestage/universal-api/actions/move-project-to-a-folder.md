# Filestage: Move Project to a Folder

Moves a Filestage project to a folder.

```
PUT https://connect.mindcloud.co/v1/universal/filestage/latest/actions/move-project-to-a-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/move-project-to-a-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "folderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/move-project-to-a-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "folderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `folderId` | string | yes | The ID of the folder to move the project into. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collaborators": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "id": "string"
      },
      "folderId": "string",
      "id": "string",
      "isArchived": true,
      "name": "Ava Chen",
      "projectTemplateId": "string",
      "sections": {
        "id": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collaborators` | array<object> |  |
| `collaborators.displayName` | string |  |
| `collaborators.email` | string |  |
| `collaborators.fullName` | string |  |
| `collaborators.id` | string |  |
| `folderId` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `name` | string |  |
| `projectTemplateId` | string |  |
| `sections` | array<object> |  |
| `sections.id` | string |  |
| `sections.name` | string |  |

## Native endpoint

Through the native Filestage API, this operation is `PUT /projects/{projectId}/folder` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-project-to-a-folder.md) for the provider-specific parameters and requirements.

