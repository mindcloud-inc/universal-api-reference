# Uploadcare: List Webhooks

Retrieves all webhooks from your Uploadcare project.

```
GET https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/list-webhooks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": 1,
      "isActive": true,
      "project": 1,
      "signingSecret": "string",
      "targetUrl": "https://example.com",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Webhook creation timestamp. |
| `event` | string | Webhook event name. |
| `id` | number | Webhook identifier. |
| `isActive` | boolean | Whether the webhook subscription is active. |
| `project` | number | Uploadcare project identifier. |
| `signingSecret` | string | Webhook signing secret when configured. |
| `targetUrl` | string | Subscribed target URL. |
| `updated` | date | Webhook update timestamp. |
| `version` | string | Webhook payload version. |

## Native endpoint

Through the native Uploadcare API, this operation is `GET /webhooks/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

