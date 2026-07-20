# Locu: Update Project

Updates an existing project in Locu.

```
PUT https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Project ID |
| `name` | string | no | New name for the project |
| `description` | string | no | Project description in markdown format |
| `icon` | string | no | New icon for the project |
| `color` | string | no | New hex color for the icon |
| `state` | string | no | New state for the project One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keepBreaks` | boolean | no | Preserve extra blank lines as empty paragraphs Default: `true`. |
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

Through the native Locu API, this operation is `PATCH /projects/:id` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

