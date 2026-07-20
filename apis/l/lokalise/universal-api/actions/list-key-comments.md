# Lokalise: List Key Comments

Retrieves comments for a Lokalise key.

```
GET https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-key-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lokalise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-key-comments?connectionId=$CONNECTION_ID&project_id=string&key_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project_id": "string",
  "key_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lokalise/latest/actions/list-key-comments?${params}`, {
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
| `project_id` | string | yes | Lokalise project identifier. |
| `key_id` | string | yes | Lokalise key identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "project_id": "string",
      "project_uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `project_id` | string |  |
| `project_uuid` | string |  |

## Native endpoint

Through the native Lokalise API, this operation is `GET /projects/:project_id/keys/:key_id/comments` (base URL `https://api.lokalise.com/api2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-key-comments.md) for the provider-specific parameters and requirements.

