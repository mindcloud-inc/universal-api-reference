# Lettr: Update Template



```
PUT https://connect.mindcloud.co/v1/universal/lettr/latest/actions/update-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/update-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/update-template', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | no | Updated HTML content. |
| `name` | string | no | Updated template name. |
| `slug` | string | yes | Template slug. |

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
        "slug": "string",
        "updated_at": "2026-05-07T12:00:00.000Z"
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
| `data` | object | Updated template payload. |
| `data.active_version` | number | Active template version after the update. |
| `data.created_at` | date | Creation timestamp. |
| `data.folder_id` | number | Folder ID. |
| `data.id` | number | Template ID. |
| `data.merge_tags` | array<object> | Detected merge tags. |
| `data.merge_tags.key` | string | Merge tag key. |
| `data.merge_tags.required` | boolean | Whether the merge tag is required. |
| `data.name` | string | Template name. |
| `data.project_id` | number | Project ID. |
| `data.slug` | string | Template slug. |
| `data.updated_at` | date | Last update timestamp. |
| `message` | string | Template update status message. |

## Native endpoint

Through the native Lettr API, this operation is `PUT /templates/:slug` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-template.md) for the provider-specific parameters and requirements.

