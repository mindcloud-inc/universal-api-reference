# Uploadcare: Delete Webhook

Deletes a webhook from Uploadcare by target URL.

```
DELETE https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&targetUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/delete-webhook?${params}`, {
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
| `targetUrl` | string | yes | Webhook destination URL to unsubscribe. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Uploadcare API returns.

## Native endpoint

Through the native Uploadcare API, this operation is `DELETE /webhooks/unsubscribe/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

