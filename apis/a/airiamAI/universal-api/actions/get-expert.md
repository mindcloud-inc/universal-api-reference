# Airiam AI: Get Expert

Retrieves an expert from Airiam AI.

```
GET https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/get-expert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/get-expert?connectionId=$CONNECTION_ID&plusId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "plusId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/get-expert?${params}`, {
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
| `plusId` | string | yes | Expert identifier from the Airiam plus endpoint. |

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

Through the native Airiam AI API, this operation is `GET /api/v1/plus/:plusId` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expert.md) for the provider-specific parameters and requirements.

