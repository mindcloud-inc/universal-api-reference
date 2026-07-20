# Lettr: Create Template



```
POST https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | HTML content for the template. |
| `name` | string | yes | Template name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "active_version": 1,
        "created_at": "2026-05-07T12:00:00.000Z",
        "folder_id": 1,
        "id": 1,
        "merge_tags": {
          "key": "string",
          "required": true
        },
        "name": "Ava Chen",
        "project_id": 1,
        "slug": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Created template payload. |
| `data.active_version` | number | Active template version. |
| `data.created_at` | date | Creation timestamp. |
| `data.folder_id` | number | Folder ID. |
| `data.id` | number | Template ID. |
| `data.merge_tags` | array<object> | Detected merge tags. |
| `data.merge_tags.key` | string | Merge tag key. |
| `data.merge_tags.required` | boolean | Whether the merge tag is required. |
| `data.name` | string | Template name. |
| `data.project_id` | number | Project ID. |
| `data.slug` | string | Template slug. |
| `message` | string | Template creation status message. |

## Native endpoint

Through the native Lettr API, this operation is `POST /templates` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

