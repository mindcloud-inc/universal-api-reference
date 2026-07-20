# Anthropic: List Skill Versions

Retrieves versions for an Anthropic skill.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-skill-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-skill-versions?connectionId=$CONNECTION_ID&skillId=skill_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "skillId": "skill_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-skill-versions?${params}`, {
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
| `skillId` | string | yes | Identifier of the skill whose versions to list. Example: `skill_abc123`. |
| `limit` | number | no | Maximum number of versions to return. Example: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | string | no | Opaque page token for pagination. Example: `page_MjAyNS0wMS0wMVQwMDowMDowMFo=`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true,
      "nextPage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of skill versions. |
| `hasMore` | boolean | Whether more pages are available. |
| `nextPage` | string | Opaque token for the next page. |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/skills/:skill_id/versions` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-skill-versions.md) for the provider-specific parameters and requirements.

