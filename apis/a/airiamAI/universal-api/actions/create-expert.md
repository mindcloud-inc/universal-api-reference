# Airiam AI: Create Expert

Creates or updates an expert in Airiam AI.

```
POST https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/create-expert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/create-expert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/create-expert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "context": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "files": [
        {}
      ],
      "id": "string",
      "isPublic": true,
      "title": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | string | Context of the Plus entry. |
| `created` | date | Creation timestamp. |
| `description` | string | Description of the Plus entry. |
| `files` | array<object> | Associated files. |
| `id` | string | Unique identifier for the Plus entry. |
| `isPublic` | boolean | Whether the entry is public. |
| `title` | string | Title of the Plus entry. |
| `userId` | number | ID of the user who created the entry. |

## Native endpoint

Through the native Airiam AI API, this operation is `POST /api/v1/plus` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expert.md) for the provider-specific parameters and requirements.

