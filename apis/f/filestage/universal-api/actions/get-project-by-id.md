# Filestage: Get Project by ID

Retrieves a project from Filestage by ID.

```
GET https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-project-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-project-by-id?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/filestage/latest/actions/get-project-by-id?${params}`, {
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
| `projectId` | string | yes | Project Id |

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

Through the native Filestage API, this operation is `GET /projects/{projectId}` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-id.md) for the provider-specific parameters and requirements.

