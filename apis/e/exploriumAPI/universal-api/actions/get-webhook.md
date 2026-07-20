# Explorium: Get Webhook

Retrieves a webhook from Explorium API.

```
GET https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explorium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-webhook?connectionId=$CONNECTION_ID&partner_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "partner_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-webhook?${params}`, {
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
| `partner_id` | string | yes | Webhook partner identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "responseContext": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `responseContext` | object | Raw API response context. |

## Native endpoint

Through the native Explorium API, this operation is `GET /v1/webhooks/{{partner_id}}` (base URL `https://api.explorium.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

