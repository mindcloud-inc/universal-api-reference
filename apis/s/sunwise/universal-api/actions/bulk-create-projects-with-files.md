# Sunwise: Bulk Create Projects With Files

Creates multiple projects from uploaded files in Sunwise.

```
POST https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/bulk-create-projects-with-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/bulk-create-projects-with-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "string",
  "contact_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/bulk-create-projects-with-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files": "string",
    "contact_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `files` | file<file> | yes |  |
| `contact_id` | string | yes |  |
| `pre_group_files` | boolean | no | Default: `true`. |
| `background_project_stop` | number | no | Default: `-1`. |
| `project_names_map` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Sunwise API, this operation is `POST /projects/bulk-create` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-create-projects-with-files.md) for the provider-specific parameters and requirements.

