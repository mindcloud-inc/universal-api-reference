# Simplecast: List Episode Keywords

Retrieves keywords for an episode from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-episode-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-episode-keywords?connectionId=$CONNECTION_ID&episodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "episodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-episode-keywords?${params}`, {
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
| `episodeId` | string | yes | Simplecast episode identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ],
      "href": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> |  |
| `href` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Simplecast API, this operation is `GET /episodes/:episode_id/keywords` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episode-keywords.md) for the provider-specific parameters and requirements.

