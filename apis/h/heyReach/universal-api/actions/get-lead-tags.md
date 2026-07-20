# Hey Reach: Get Lead Tags

Retrieves tags for a lead in Hey Reach.

```
GET https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-lead-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hey Reach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-lead-tags?connectionId=$CONNECTION_ID&profileUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "profileUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/get-lead-tags?${params}`, {
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
| `profileUrl` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags` | array<string> |  |

## Native endpoint

Through the native Hey Reach API, this operation is `POST /api/public/lead/GetTags` (base URL `https://api.heyreach.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-tags.md) for the provider-specific parameters and requirements.

