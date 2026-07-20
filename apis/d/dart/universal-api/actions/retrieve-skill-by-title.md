# Dart: Retrieve Skill by Title

Retrieves a skill from Dart by title.

```
GET https://connect.mindcloud.co/v1/universal/dart/latest/actions/retrieve-skill-by-title
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/retrieve-skill-by-title?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/retrieve-skill-by-title?${params}`, {
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
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "promptMarkdown": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `promptMarkdown` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Dart API, this operation is `GET /skills/by-title` (base URL `https://app.dartai.com/api/v0/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-skill-by-title.md) for the provider-specific parameters and requirements.

