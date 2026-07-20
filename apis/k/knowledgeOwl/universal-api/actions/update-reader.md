# KnowledgeOwl: Update Reader



```
PUT https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-reader
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-reader" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/update-reader', {
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
| `id` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `status` | string | no | Default: `active`. |

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

Through the native KnowledgeOwl API, this operation is `PUT /reader/:id.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reader.md) for the provider-specific parameters and requirements.

