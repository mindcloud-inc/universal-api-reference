# Responsr: Get Project Webhook



```
GET https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-project-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Responsr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-project-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/responsr/latest/actions/get-project-webhook?${params}`, {
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
| `id` | string | no | Responsr webhook ID. |
| `projectId` | string | no | Responsr project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventType": "string",
      "id": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventType` | string |  |
| `id` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Responsr API, this operation is `GET /api/v1.0/projects/:projectId/webhooks/:id` (base URL `https://app.responsr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-webhook.md) for the provider-specific parameters and requirements.

