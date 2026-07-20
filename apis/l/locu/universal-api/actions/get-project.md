# Locu: Get Project

Retrieves a single project by ID from Locu.

```
GET https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | Project ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeHtml` | boolean | no | Include description content as HTML |
| `includeMarkdown` | boolean | no | Include description content as Markdown |
| `includePlainText` | boolean | no | Include description content as plain text |
| `includeJson` | boolean | no | Include description content as structured JSON |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "icon": "string",
      "id": "string",
      "name": "Ava Chen",
      "state": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Project icon color |
| `completedAt` | date | Project completion timestamp |
| `createdAt` | date | Project creation timestamp |
| `icon` | string | Project icon |
| `id` | string | Project ID |
| `name` | string | Project name |
| `state` | string | Project state |
| `updatedAt` | date | Project last update timestamp |

## Native endpoint

Through the native Locu API, this operation is `GET /projects/:id` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

