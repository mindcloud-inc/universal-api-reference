# Vooplayer: Get Video Views

Retrieves video view records from Vooplayer.

```
GET https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/get-video-views
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vooplayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/get-video-views?connectionId=$CONNECTION_ID&videoId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vooplayer/latest/actions/get-video-views?${params}`, {
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
| `videoId` | number | yes | Video metrics ID. |
| `customViewerId` | string | no | ID or email of a known viewer. |
| `onlyWatched` | boolean | no | Return only views with percentWatched greater than 1. |
| `allViews` | boolean | no | Disable data pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "data": [
        {}
      ],
      "from": 1,
      "last_page": 1,
      "next_page_url": "https://example.com",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "summary": {
        "totalTime": 1
      },
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number | Current page number. |
| `data` | array<object> | View records. |
| `from` | number | First row position in this page when available. |
| `last_page` | number | Last page number. |
| `next_page_url` | string | Next page URL when available. |
| `per_page` | number | Page size. |
| `prev_page_url` | string | Previous page URL when available. |
| `summary` | object | Summary metrics object. |
| `summary.totalTime` | number | Total watched time across matched views. |
| `to` | number | Last row position in this page when available. |
| `total` | number | Total views returned by the query. |

## Native endpoint

Through the native Vooplayer API, this operation is `GET /api/views/getViews` (base URL `https://api.spotlightr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-views.md) for the provider-specific parameters and requirements.

