# Umami: Get Website Metrics



```
GET https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umami `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-metrics?connectionId=$CONNECTION_ID&limit=25&offset=0&websiteId=string&startAt=1&endAt=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "websiteId": "string",
  "startAt": "1",
  "endAt": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umami/latest/actions/get-website-metrics?${params}`, {
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
| `type` | string | no | Metric type to group by. One of: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "x": "string",
      "y": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `x` | string | Metric bucket label. |
| `y` | number | Metric value. |

## Native endpoint

Through the native Umami API, this operation is `GET /websites/:websiteId/metrics` (base URL `https://api.umami.is/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-website-metrics.md) for the provider-specific parameters and requirements.

