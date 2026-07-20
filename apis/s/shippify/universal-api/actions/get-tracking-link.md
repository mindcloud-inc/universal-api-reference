# Shippify: Get Tracking Link

Retrieves a secure delivery tracking link from Shippify.

```
GET https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-tracking-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-tracking-link?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shippify/latest/actions/get-tracking-link?${params}`, {
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
| `id` | string | yes | Shippify delivery identifier or reference ID to retrieve the tracking link for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recipient": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recipient.email` | string | Recipient email. |
| `recipient.name` | string | Recipient name. |
| `token` | string | Tracking token. |
| `url` | string | Tracking URL. |

## Native endpoint

Through the native Shippify API, this operation is `GET /v1/deliveries/token/:id` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking-link.md) for the provider-specific parameters and requirements.

