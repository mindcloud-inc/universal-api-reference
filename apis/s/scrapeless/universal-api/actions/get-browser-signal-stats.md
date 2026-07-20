# Scrapeless: Get Browser Signal Stats

Retrieves browser signal stats from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-signal-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-signal-stats?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-browser-signal-stats?${params}`, {
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
| `taskId` | string | yes |  |
| `xApiToken` | string | no | API Key |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": 1,
      "status": 1,
      "waiters": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | number | Number of events |
| `status` | number |  |
| `waiters` | number | Number of waiters |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /browser/:taskId/signal/stats` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-browser-signal-stats.md) for the provider-specific parameters and requirements.

