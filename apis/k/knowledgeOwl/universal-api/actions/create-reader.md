# KnowledgeOwl: Create Reader



```
POST https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-reader
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KnowledgeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-reader" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tempPass": "string",
  "pwType": "temp",
  "username": "Ava Chen",
  "status": "active",
  "projects[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/create-reader', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tempPass": "string",
    "pwType": "temp",
    "username": "Ava Chen",
    "status": "active",
    "projects[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tempPass` | string | yes |  |
| `pwType` | string | yes | Default: `temp`. |
| `username` | string | yes |  |
| `status` | string | yes | Default: `active`. |
| `projects[]` | array<string> | yes |  |

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

Through the native KnowledgeOwl API, this operation is `POST /reader.json` (base URL `https://app.knowledgeowl.com/api/head`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reader.md) for the provider-specific parameters and requirements.

