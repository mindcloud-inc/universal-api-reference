# Crime Junkie Podcast: Get Author

Retrieves an author from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-author
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-author?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-author?${params}`, {
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
| `id` | string | yes | The author id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrls": {},
      "description": "string",
      "id": 1,
      "link": "https://example.com",
      "name": "Ava Chen",
      "slug": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrls` | object |  |
| `description` | string |  |
| `id` | number |  |
| `link` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /wp-json/wp/v2/users/:id` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-author.md) for the provider-specific parameters and requirements.

