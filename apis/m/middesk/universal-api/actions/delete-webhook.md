# Middesk: Delete a webhook

Deletes a webhook from your Middesk account.

```
DELETE https://connect.mindcloud.co/v1/universal/middesk/latest/actions/delete-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/delete-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/delete-webhook?${params}`, {
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
| `id` | string | yes | ID of the webhook to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "disabledAt": "string",
      "enabledEvents": [
        "string"
      ],
      "id": "string",
      "oauthClientId": "string",
      "object": "string",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Webhook creation timestamp. |
| `disabledAt` | string | Webhook disabled timestamp, when present. |
| `enabledEvents` | array<string> | Events currently enabled for this webhook. |
| `id` | string | Webhook identifier. |
| `oauthClientId` | string | OIDC OAuth client ID when configured. |
| `object` | string | Type of resource returned by Middesk. |
| `updatedAt` | string | Webhook update timestamp. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native Middesk API, this operation is `DELETE /webhooks/:id` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook.md) for the provider-specific parameters and requirements.

