# Lettr: Get Template



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-template?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/get-template?${params}`, {
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
        "html": "string",
        "id": 1,
        "json": {},
        "name": "Ava Chen",
        "project_id": 1,
        "slug": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "versions_count": 1
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
| `data` | object | Template payload. |
| `data.active_version` | number | Active template version. |
| `data.created_at` | date | Creation timestamp. |
| `data.folder_id` | number | Folder ID. |
| `data.html` | string | HTML template content. |
| `data.id` | number | Template ID. |
| `data.json` | object | Visual editor JSON content when present. |
| `data.name` | string | Template name. |
| `data.project_id` | number | Project ID. |
| `data.slug` | string | Template slug. |
| `data.updated_at` | date | Last update timestamp. |
| `data.versions_count` | number | Number of versions. |
| `message` | string | Template retrieval status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /templates/:slug` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

