# Umami: Get Website Stats



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-stats?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-stats?${params}`, {
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
| `websiteId` | string | yes | The website ID. |
| `startAt` | number | yes | Start timestamp in milliseconds. |
| `endAt` | number | yes | End timestamp in milliseconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bounces": 1,
      "comparison": {},
      "pageviews": 1,
      "totaltime": 1,
      "visitors": 1,
      "visits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bounces` | number | Total bounces in the selected range. |
| `comparison` | object | Comparison totals for the previous comparison window. |
| `pageviews` | number | Total pageviews in the selected range. |
| `totaltime` | number | Total time spent on the website. |
| `visitors` | number | Total unique visitors in the selected range. |
| `visits` | number | Total visits in the selected range. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/stats` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-stats.md) for the provider-specific parameters and requirements.

