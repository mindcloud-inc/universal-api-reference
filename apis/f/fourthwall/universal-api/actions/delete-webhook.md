# Fourthwall: Delete Webhook

Deletes an existing webhook from Fourthwall.

```
DELETE https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&webhookConfigurationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookConfigurationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/delete-webhook?${params}`, {
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
| `webhookConfigurationId` | string | yes | The webhook configuration ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fourthwall API returns.

## Native endpoint

Through the native Fourthwall API, this operation is `DELETE /open-api/v1.0/webhooks/:webhookConfigurationId` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

