# Filestage: Add New Section

Creates a new section in a Filestage project.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-new-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-new-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "sectionName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/add-new-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "sectionName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project Id |
| `sectionName` | string | yes |  |

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

Through the native Filestage API, this operation is `POST /projects/{projectId}/sections` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-new-section.md) for the provider-specific parameters and requirements.

