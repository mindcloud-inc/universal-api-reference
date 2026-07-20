# Crime Junkie Podcast: Get Content Type

Retrieves a content type from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-content-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-content-type?connectionId=$CONNECTION_ID&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-content-type?${params}`, {
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
| `type` | string | yes | The WordPress content type slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "hasArchive": true,
      "hierarchical": true,
      "name": "Ava Chen",
      "restBase": "string",
      "restNamespace": "Ava Chen",
      "slug": "string",
      "taxonomies": [
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
| `description` | string |  |
| `hasArchive` | boolean |  |
| `hierarchical` | boolean |  |
| `name` | string |  |
| `restBase` | string |  |
| `restNamespace` | string |  |
| `slug` | string |  |
| `taxonomies` | array<string> |  |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /wp-json/wp/v2/types/:type` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-type.md) for the provider-specific parameters and requirements.

