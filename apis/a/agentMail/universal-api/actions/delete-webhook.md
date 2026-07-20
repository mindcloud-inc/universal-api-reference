# Agent Mail: Delete Webhook

Deletes an existing webhook from AgentMail.

```
DELETE https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/delete-webhook?${params}`, {
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
| `webhookId` | string | yes | The AgentMail webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Successful no-body response acknowledged by the wrapper. |

## Native endpoint

Through the native Agent Mail API, this operation is `DELETE /webhooks/{webhook_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

