# Crime Junkie Podcast: List Statuses

Retrieves statuses from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "dateFloating": true,
      "key": "string",
      "name": "Ava Chen",
      "public": true,
      "queryable": true,
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateFloating` | boolean |  |
| `key` | string |  |
| `name` | string |  |
| `public` | boolean |  |
| `queryable` | boolean |  |
| `slug` | string |  |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /wp-json/wp/v2/statuses` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-statuses.md) for the provider-specific parameters and requirements.

