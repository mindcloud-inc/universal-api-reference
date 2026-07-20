# SignRequest: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignRequest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-webhook?connectionId=$CONNECTION_ID&uuid=2cb9cc24-7b5e-4d30-9e3f-5fbf3a9f4dc9" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "2cb9cc24-7b5e-4d30-9e3f-5fbf3a9f4dc9"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signRequest/latest/actions/get-webhook?${params}`, {
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
| `uuid` | string | yes | Example: `2cb9cc24-7b5e-4d30-9e3f-5fbf3a9f4dc9`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "created": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "integration": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `created` | date |  |
| `eventType` | string |  |
| `integration` | string |  |
| `name` | string |  |
| `url` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SignRequest API, this operation is `GET /webhooks/:uuid/` (base URL `https://signrequest.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

