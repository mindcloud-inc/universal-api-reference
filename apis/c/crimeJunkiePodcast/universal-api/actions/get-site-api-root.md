# Crime Junkie Podcast: Get Site API Root

Retrieves the site API root from Crime Junkie Podcast.

```
GET https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-site-api-root
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Crime Junkie Podcast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-site-api-root?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/get-site-api-root?${params}`, {
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
      "description": "string",
      "gmtOffset": 1,
      "home": "string",
      "name": "Ava Chen",
      "namespaces": [
        "Ava Chen"
      ],
      "routes": {},
      "timezoneString": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `gmtOffset` | number |  |
| `home` | string |  |
| `name` | string |  |
| `namespaces` | array<string> |  |
| `routes` | object |  |
| `timezoneString` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Crime Junkie Podcast API, this operation is `GET /wp-json/` (base URL `https://crimejunkiepodcast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-site-api-root.md) for the provider-specific parameters and requirements.

