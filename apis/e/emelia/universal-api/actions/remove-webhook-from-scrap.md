# Emelia: Remove Webhook From Scrap

Deletes a webhook from a scrap in Emelia.

```
DELETE https://connect.mindcloud.co/v1/universal/emelia/latest/actions/remove-webhook-from-scrap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emelia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/emelia/latest/actions/remove-webhook-from-scrap?connectionId=$CONNECTION_ID&id=string&webhookUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "webhookUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emelia/latest/actions/remove-webhook-from-scrap?${params}`, {
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
| `id` | string | yes | Scrap identifier |
| `webhookUrl` | string | yes | Webhook URL |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "removeWebhookFromScrap": {}
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.removeWebhookFromScrap` | object |  |

## Native endpoint

Through the native Emelia API, this operation is `POST /graphql` (base URL `https://graphql.emelia.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-webhook-from-scrap.md) for the provider-specific parameters and requirements.

