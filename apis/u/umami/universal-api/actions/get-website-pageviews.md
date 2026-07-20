# Umami: Get Website Pageviews



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-pageviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-pageviews?connectionId=$CONNECTION_ID&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-pageviews?${params}`, {
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
| `unit` | string | no | Time bucket unit. One of: `0`, `1`, `2`, `3`. |
| `timezone` | string | no | Timezone like America/Los_Angeles. |
| `compare` | string | no | Comparison period. One of: `0`, `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageviews": [
        {}
      ],
      "sessions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageviews` | array<object> | Time-series pageview points. |
| `sessions` | array<object> | Time-series session points. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/pageviews` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-website-pageviews.md) for the provider-specific parameters and requirements.

