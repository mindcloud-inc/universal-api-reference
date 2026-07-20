# KnowledgeOwl: Get File



```
GET https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/get-file?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/get-file?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "contentType": "string",
        "date_created": "2026-05-07T12:00:00.000Z",
        "date_deleted": "2026-05-07T12:00:00.000Z",
        "date_modified": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": "string",
        "length": 1,
        "md5": "string",
        "name": "Ava Chen",
        "project_id": "string",
        "status": "string",
        "tags": [
          [
            "string"
          ]
        ],
        "thumbnail": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.contentType` | string |  |
| `data.date_created` | date |  |
| `data.date_deleted` | date |  |
| `data.date_modified` | date |  |
| `data.description` | string |  |
| `data.id` | string |  |
| `data.length` | number |  |
| `data.md5` | string |  |
| `data.name` | string |  |
| `data.project_id` | string |  |
| `data.status` | string |  |
| `data.tags[]` | array<string> |  |
| `data.thumbnail` | string |  |
| `data.type` | string |  |
| `data.url` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native KnowledgeOwl API, this operation is `GET /file/:id.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

