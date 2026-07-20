# Webex: List Webhooks

Lists webhooks in your Webex account.

```
GET https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webex/latest/actions/list-webhooks?${params}`, {
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
| `max` | number | no | Maximum number of webhooks to return. Example: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "event": "string",
      "filter": "string",
      "id": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "ownedBy": "string",
      "resource": "string",
      "status": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | Webex app identifier associated with the webhook. |
| `created` | date | Webhook creation timestamp. |
| `createdBy` | string | Person identifier that created the webhook. |
| `event` | string | Event type the webhook listens to. |
| `filter` | string | Optional event filter expression. |
| `id` | string | Webhook identifier. |
| `name` | string | Webhook display name. |
| `orgId` | string | Organization identifier for the webhook. |
| `ownedBy` | string | Webhook ownership scope. |
| `resource` | string | Resource type the webhook listens to. |
| `status` | string | Webhook status. |
| `targetUrl` | string | HTTPS endpoint that receives webhook notifications. |

## Native endpoint

Through the native Webex API, this operation is `GET /webhooks` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

