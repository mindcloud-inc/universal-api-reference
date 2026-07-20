# EODHD: List Financial News

Retrieves financial news for symbols or tags from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-financial-news
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-financial-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-financial-news?${params}`, {
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
| `s` | string | no | Comma-separated symbols, for example AAPL.US. Example: `AAPL.US`. |
| `offset` | number | no | Number of news items to skip. Example: `0`. |
| `limit` | number | no | Maximum number of news items to return. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "link": "https://example.com",
      "sentiment": {},
      "symbols": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string | Article content or excerpt. |
| `date` | date | Published date. |
| `link` | string | Article URL. |
| `sentiment` | object | Article sentiment metadata. |
| `symbols` | array<string> | Related symbols. |
| `tags` | array<string> | Related tags. |
| `title` | string | Article title. |

## Native endpoint

Through the native EODHD API, this operation is `GET /news` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-financial-news.md) for the provider-specific parameters and requirements.

