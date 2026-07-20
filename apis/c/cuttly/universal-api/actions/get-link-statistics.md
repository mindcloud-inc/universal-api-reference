# Cutt.ly: Get Link Statistics

Retrieves click statistics for a shortened link in Cutt.ly.

```
GET https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/get-link-statistics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cutt.ly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/get-link-statistics?connectionId=$CONNECTION_ID&stats=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stats": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cuttly/latest/actions/get-link-statistics?${params}`, {
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
| `stats` | string | yes | The short link whose analytics you want to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bots": "string",
      "clicks": 1,
      "date": "string",
      "devices": {},
      "facebook": 1,
      "fullLink": "https://example.com",
      "googlePlus": 1,
      "instagram": 1,
      "linkedin": 1,
      "pinterest": 1,
      "refs": {},
      "rest": 1,
      "shortLink": "https://example.com",
      "status": 1,
      "title": "string",
      "twitter": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bots` | string | Bot-click count or provider message when bot analytics are unavailable for the current plan. |
| `clicks` | number | Total number of clicks. |
| `date` | string | Date the short link was created. |
| `devices` | object | Device-level analytics map when available. |
| `facebook` | number | Clicks attributed to Facebook. |
| `fullLink` | string | Original destination URL. |
| `googlePlus` | number | Clicks attributed to Google Plus. |
| `instagram` | number | Clicks attributed to Instagram. |
| `linkedin` | number | Clicks attributed to LinkedIn. |
| `pinterest` | number | Clicks attributed to Pinterest. |
| `refs` | object | Referrer analytics map when available. |
| `rest` | number | Clicks from other referrers. |
| `shortLink` | string | Shortened URL. |
| `status` | number | Provider status code for the statistics request. |
| `title` | string | Stored title for the short link. |
| `twitter` | number | Clicks attributed to Twitter. |

## Native endpoint

Through the native Cutt.ly API, this operation is `GET /api.php` (base URL `https://cutt.ly/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-link-statistics.md) for the provider-specific parameters and requirements.

