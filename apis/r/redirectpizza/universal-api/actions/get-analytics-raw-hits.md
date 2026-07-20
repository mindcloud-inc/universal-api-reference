# redirect.pizza: Get Analytics Raw Hits



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-raw-hits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-raw-hits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-raw-hits?${params}`, {
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
| `start` | string | no | Start date or timestamp for the analytics window. |
| `end` | string | no | End date or timestamp for the analytics window. |
| `query` | string | no | Filter expression for analytics results. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Cursor token for the next page of raw analytics results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browserName": "Ava Chen",
      "city": "string",
      "continent": "string",
      "continentName": "Ava Chen",
      "country": "string",
      "createdAt": "string",
      "destinationUrl": "https://example.com",
      "deviceType": "string",
      "fullUrl": "https://example.com",
      "id": 1,
      "ip": "string",
      "isCrawler": true,
      "method": "string",
      "operatingSystem": "string",
      "platform": "string",
      "redirectId": 1,
      "redirectType": "string",
      "referer": "string",
      "refererHost": "string",
      "scheme": "string",
      "subdivisionCode": "string",
      "subdivisionName": "Ava Chen",
      "tracking": true,
      "userAgent": "string",
      "wafBlocked": true,
      "wafRules": [
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
| `browserName` | string |  |
| `city` | string |  |
| `continent` | string |  |
| `continentName` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `destinationUrl` | string |  |
| `deviceType` | string |  |
| `fullUrl` | string |  |
| `id` | number |  |
| `ip` | string |  |
| `isCrawler` | boolean |  |
| `method` | string |  |
| `operatingSystem` | string |  |
| `platform` | string |  |
| `redirectId` | number |  |
| `redirectType` | string |  |
| `referer` | string |  |
| `refererHost` | string |  |
| `scheme` | string |  |
| `subdivisionCode` | string |  |
| `subdivisionName` | string |  |
| `tracking` | boolean |  |
| `userAgent` | string |  |
| `wafBlocked` | boolean |  |
| `wafRules` | array<string> |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/analytics/raw` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-raw-hits.md) for the provider-specific parameters and requirements.

