# Anthropic: List Skills

Retrieves skills from the Anthropic account.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-skills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-skills?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-skills?${params}`, {
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
| `limit` | number | no | Maximum number of skills to return. Example: `20`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | string | no | Opaque page token for pagination. Example: `page_MjAyNS0wMS0wMVQwMDowMDowMFo=`. |
| `source` | string | no | Optional source filter (for example user or system). Example: `user`. |

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
| `data` | array<object> | List of skills. |
| `hasMore` | boolean | Whether more pages are available. |
| `nextPage` | string | Opaque token for the next page. |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/skills` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-skills.md) for the provider-specific parameters and requirements.

