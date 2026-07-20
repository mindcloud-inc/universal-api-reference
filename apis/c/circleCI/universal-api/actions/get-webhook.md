# CircleCI: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CircleCI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-webhook?connectionId=$CONNECTION_ID&webhook_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhook_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/circleCI/latest/actions/get-webhook?${params}`, {
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
| `webhook_id` | string | yes | Opaque webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "url": "https://example.com",
      "verifyTls": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `url` | string |  |
| `verifyTls` | boolean |  |

## Native endpoint

Through the native CircleCI API, this operation is `GET /webhook/:webhook_id` (base URL `https://circleci.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

