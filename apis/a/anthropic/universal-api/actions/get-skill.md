# Anthropic: Get Skill

Retrieves a specific skill from Anthropic.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-skill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-skill?connectionId=$CONNECTION_ID&skillId=skill_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "skillId": "skill_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/get-skill?${params}`, {
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
| `skillId` | string | yes | Identifier of the skill to retrieve. Example: `skill_abc123`. |

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

Through the native Anthropic API, this operation is `GET /v1/skills/:skill_id` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-skill.md) for the provider-specific parameters and requirements.

