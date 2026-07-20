# Hireflix: List Position Questions

Retrieves interview questions for a position in Hireflix.

```
GET https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-questions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hireflix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-questions?connectionId=$CONNECTION_ID&variables.id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hireflix/latest/actions/list-position-questions?${params}`, {
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
| `variables.id` | string | yes | The Hireflix position ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": "string",
      "media": {
        "createdAt": 1,
        "id": "string",
        "thumbnail": "string",
        "type": "string",
        "url": "https://example.com"
      },
      "notes": "string",
      "retakes": 1,
      "timeToAnswer": 1,
      "timeToThink": 1,
      "title": "string",
      "transcriptionLanguage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `media.createdAt` | number |  |
| `media.id` | string |  |
| `media.thumbnail` | string |  |
| `media.type` | string |  |
| `media.url` | string |  |
| `notes` | string |  |
| `retakes` | number |  |
| `timeToAnswer` | number |  |
| `timeToThink` | number |  |
| `title` | string |  |
| `transcriptionLanguage` | string |  |

## Native endpoint

Through the native Hireflix API, this operation is `POST me` (base URL `https://api.hireflix.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-position-questions.md) for the provider-specific parameters and requirements.

