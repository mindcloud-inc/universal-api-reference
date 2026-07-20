# Avaza: Delete Webhook By URL

Deletes a webhook from Avaza by callback URL.

```
DELETE https://connect.mindcloud.co/v1/universal/avaza/latest/actions/delete-webhook-by-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/delete-webhook-by-url?connectionId=$CONNECTION_ID&targetUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/delete-webhook-by-url?${params}`, {
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
| `targetUrl` | string | yes | Target URL that should be used to delete subscriptions |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `DELETE /api/Webhook` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-by-url.md) for the provider-specific parameters and requirements.

