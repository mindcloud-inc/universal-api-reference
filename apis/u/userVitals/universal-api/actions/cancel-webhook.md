# UserVitals: Cancel Webhook

Cancels a webhook in the roadmap API.

```
DELETE https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/cancel-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/cancel-webhook?connectionId=$CONNECTION_ID&targetUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/cancel-webhook?${params}`, {
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
| `targetUrl` | string | yes | The webhook target URL. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `POST /webhooks/cancel` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-webhook.md) for the provider-specific parameters and requirements.

