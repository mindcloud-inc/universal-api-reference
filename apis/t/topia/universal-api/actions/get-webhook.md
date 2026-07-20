# Topia: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Topia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-webhook?connectionId=$CONNECTION_ID&urlSlug=https%3A%2F%2Fexample.com&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlSlug": "https://example.com",
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topia/latest/actions/get-webhook?${params}`, {
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
| `urlSlug` | string | yes | Topia world URL slug. |
| `webhookId` | string | yes | Identifier for the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "assetId": "string",
      "dateAdded": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "isUniqueOnly": true,
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "urlSlug": "https://example.com",
      "webhookId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `assetId` | string |  |
| `dateAdded` | date |  |
| `description` | string |  |
| `isUniqueOnly` | boolean |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `urlSlug` | string |  |
| `webhookId` | string |  |

## Native endpoint

Through the native Topia API, this operation is `GET /v1/world/:urlSlug/webhooks/:webhookId` (base URL `https://api.topia.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

