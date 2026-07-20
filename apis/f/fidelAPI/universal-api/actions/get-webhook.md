# Fidel API: Get Webhook

Retrieves a webhook from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-webhook?connectionId=$CONNECTION_ID&hookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/get-webhook?${params}`, {
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
| `hookId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": "string",
      "live": true,
      "programId": "string",
      "secretKey": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `created` | date |  |
| `event` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `programId` | string |  |
| `secretKey` | string |  |
| `updated` | date |  |
| `url` | string |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /hooks/:hookId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

