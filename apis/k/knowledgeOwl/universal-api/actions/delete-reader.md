# KnowledgeOwl: Delete Reader



```
DELETE https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/delete-reader
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/delete-reader?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/delete-reader?${params}`, {
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
        "first_name": "Ava",
        "id": "string",
        "last_name": "Chen",
        "projects": [
          [
            "string"
          ]
        ],
        "status": "string",
        "type": "string",
        "username": "Ava Chen"
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
| `data.first_name` | string |  |
| `data.id` | string |  |
| `data.last_name` | string |  |
| `data.projects[]` | array |  |
| `data.status` | string |  |
| `data.type` | string |  |
| `data.username` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native KnowledgeOwl API, this operation is `DELETE /reader/:id.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-reader.md) for the provider-specific parameters and requirements.

