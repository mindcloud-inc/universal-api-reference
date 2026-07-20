# Scrapeless: Clear Browser Signals

Deletes browser signals from Scrapeless.

```
DELETE https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/clear-browser-signals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/clear-browser-signals?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/clear-browser-signals?${params}`, {
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
| `taskId` | string | yes | session task id |
| `xApiToken` | string | no | API Key |
| `event` | string | no | Event name, if not provided, all events will be cleared |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scrapeless API returns.

## Native endpoint

Through the native Scrapeless API, this operation is `DELETE /browser/:taskId/signal/clear` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-browser-signals.md) for the provider-specific parameters and requirements.

