# Zoominfo: List News

Finds news in ZoomInfo by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-news?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/list-news?${params}`, {
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
| `categories[]` | array<string> | no | Category of news articles. Accepts an Array of String. See the 'News Categories' endpoint for values. |
| `url[]` | array<string> | no | Search news by URL strings. Accepts an Array of String. Minimum of 5 characters per input |
| `pageDateMin` | string | no | Specify the earliest publishing date for news articles returned. For example, 2020-01-01 will return all news articles published on or after Jan 1, 2020. |
| `pageDateMax` | string | no | Specify the latest publishing date for news articles articles. For example, 2020-01-31 will return all new articles published on or before Jan 31, 2020. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": [
        "string"
      ],
      "company": [
        {}
      ],
      "description": "string",
      "domain": "string",
      "imageUrl": "https://example.com",
      "pageDate": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<string> |  |
| `company` | array<object> |  |
| `description` | string |  |
| `domain` | string |  |
| `imageUrl` | string |  |
| `pageDate` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Zoominfo API, this operation is `POST search/news` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-news.md) for the provider-specific parameters and requirements.

