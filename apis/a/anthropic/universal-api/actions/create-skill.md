# Anthropic: Create Skill

Creates a new skill in Anthropic.

```
POST https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-skill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-skill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files": "file_abc123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/create-skill', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files": "file_abc123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `displayTitle` | string | no | Optional human-readable title for the skill. Example: `My Skill`. |
| `files` | list<string> | yes | Files to upload as skill inputs (multipart UploadFile fields). Example: `file_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Skill identifier. |
| `name` | string | Skill name. |
| `type` | string | Object type. |

## Native endpoint

Through the native Anthropic API, this operation is `POST /v1/skills` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-skill.md) for the provider-specific parameters and requirements.

