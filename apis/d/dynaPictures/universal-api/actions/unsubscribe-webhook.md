# DynaPictures: Unsubscribe Webhook

Deletes a webhook subscription from DynaPictures.

```
DELETE https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/unsubscribe-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynaPictures `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/unsubscribe-webhook?connectionId=$CONNECTION_ID&targetUrl=https%3A%2F%2Fexample.com&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targetUrl": "https://example.com",
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynaPictures/latest/actions/unsubscribe-webhook?${params}`, {
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
| `targetUrl` | string | yes | Webhook URL that receives notifications. |
| `templateId` | string | yes | UID of the template to stop watching. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynaPictures API returns.

## Native endpoint

Through the native DynaPictures API, this operation is `DELETE /hooks` (base URL `https://api.dynapictures.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-webhook.md) for the provider-specific parameters and requirements.

