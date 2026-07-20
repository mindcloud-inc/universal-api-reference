# OnceHub: Get Webhook



```
GET https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/get-webhook?${params}`, {
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
| `id` | string | yes | The OnceHub webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "secret": {},
      "status": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `creationTime` | date |  |
| `events[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `secret` | object |  |
| `status` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native OnceHub API, this operation is `GET /v2/webhooks/:id` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook.md) for the provider-specific parameters and requirements.

