# Simplecast: List Podcast Authors

Retrieves authors for a podcast from Simplecast.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcast-authors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcast-authors?connectionId=$CONNECTION_ID&podcastId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "podcastId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/list-podcast-authors?${params}`, {
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
| `podcastId` | string | yes | Simplecast podcast identifier. |

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

Through the native Simplecast API, this operation is `GET /podcasts/:podcast_id/authors` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-podcast-authors.md) for the provider-specific parameters and requirements.

