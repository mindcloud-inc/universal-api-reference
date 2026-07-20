# Crime Junkie Podcast: List Popup Makers

Retrieves popup makers from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-popup-makers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-popup-makers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-popup-makers?${params}`, {
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
      "content": {},
      "date": "2026-05-07T12:00:00.000Z",
      "dateGmt": "2026-05-07T12:00:00.000Z",
      "excerpt": {},
      "id": 1,
      "link": "https://example.com",
      "modified": "2026-05-07T12:00:00.000Z",
      "modifiedGmt": "2026-05-07T12:00:00.000Z",
      "slug": "string",
      "status": "string",
      "title": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object |  |
| `date` | date |  |
| `dateGmt` | date |  |
| `excerpt` | object |  |
| `id` | number |  |
| `link` | string |  |
| `modified` | date |  |
| `modifiedGmt` | date |  |
| `slug` | string |  |
| `status` | string |  |
| `title` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /wp-json/wp/v2/dipi_popup_maker` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-popup-makers.md) for the provider-specific parameters and requirements.

