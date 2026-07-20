# Documently: Retrieve Webhook

Retrieves a webhook from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-webhook?${params}`, {
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
| `webhookId` | string | no | The webhook id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "active": true,
      "events": [
        "string"
      ],
      "id": "string",
      "project": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `active` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `project` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Documently API, this operation is `GET /webhooks/:webhookId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook.md) for the provider-specific parameters and requirements.

