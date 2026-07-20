# Sarbacane: Get Webhook

Retrieves a webhook from your Sarbacane account.

```
GET https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sarbacane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sarbacane/latest/actions/get-webhook?${params}`, {
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
| `webhookId` | string | no | Sarbacane webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "creationDate": "string",
      "displayName": "Ava Chen",
      "id": "string",
      "kinds": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Owning account ID. |
| `creationDate` | string | Webhook creation timestamp. |
| `displayName` | string | Webhook display name. |
| `id` | string | Sarbacane webhook ID. |
| `kinds` | array<string> | Subscribed webhook event kinds. |
| `url` | string | Webhook destination URL. |

## Native endpoint

Through the native Sarbacane API, this operation is `GET /webhooks/{webhookId}` (base URL `https://api.sarbacane.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

