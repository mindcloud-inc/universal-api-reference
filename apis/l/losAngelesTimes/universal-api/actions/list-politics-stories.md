# Los Angeles Times: List Politics Stories

Retrieves Los Angeles Times politics stories.

```
GET https://connect.mindcloud.co/v1/universal/losAngelesTimes/latest/actions/list-politics-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Los Angeles Times `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/losAngelesTimes/latest/actions/list-politics-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/losAngelesTimes/latest/actions/list-politics-stories?${params}`, {
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
      "content:encoded": {},
      "dc:creator": "string",
      "description": {},
      "guid": "string",
      "link": "https://example.com",
      "media:content": {},
      "pubDate": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content:encoded` | object |  |
| `dc:creator` | string |  |
| `description` | object |  |
| `guid` | string |  |
| `link` | string |  |
| `media:content` | object |  |
| `pubDate` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Los Angeles Times API, this operation is `GET /politics/rss2.0.xml` (base URL `https://www.latimes.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-politics-stories.md) for the provider-specific parameters and requirements.

