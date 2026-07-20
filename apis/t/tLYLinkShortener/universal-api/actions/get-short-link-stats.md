# TLY Link Shortener: Get Short Link Stats

Retrieves stats for a short link in TLY Link Shortener.

```
GET https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-short-link-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-short-link-stats?connectionId=$CONNECTION_ID&shortUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/get-short-link-stats?${params}`, {
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
| `shortUrl` | string | yes | The short URL to retrieve stats for. |
| `startDate` | date | no | Optional UTC start date for the stats window. |
| `endDate` | date | no | Optional UTC end date for the stats window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browsers": [
        "string"
      ],
      "cities": [
        "string"
      ],
      "clicks": 1,
      "countries": [
        "string"
      ],
      "daily_clicks": [
        "string"
      ],
      "data": {},
      "platforms": [
        "string"
      ],
      "referrers": [
        "string"
      ],
      "total_qr_scans": 1,
      "unique_clicks": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browsers` | array |  |
| `cities` | array |  |
| `clicks` | number |  |
| `countries` | array |  |
| `daily_clicks` | array |  |
| `data` | object |  |
| `platforms` | array |  |
| `referrers` | array |  |
| `total_qr_scans` | number |  |
| `unique_clicks` | number |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `GET /api/v1/link/stats` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-short-link-stats.md) for the provider-specific parameters and requirements.

