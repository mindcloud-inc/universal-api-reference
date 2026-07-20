# Airlabs: List Flight Alert Webhook History

Retrieves flight alert webhook history from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-flight-alert-webhook-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-flight-alert-webhook-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-flight-alert-webhook-history?${params}`, {
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
| `days` | number | no | Number of days of webhook history to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listenerId` | number | no | Filter webhook history by listener ID when needed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changed": [
        "string"
      ],
      "created": "string",
      "flight": {},
      "listener_id": 1,
      "performed": "string",
      "res_headers": {},
      "res_status": 1,
      "webhook_id": 1,
      "webhook_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changed` | array<string> | Changed flight fields. |
| `created` | string | Webhook creation date. |
| `flight` | object | Flight payload sent to the webhook. |
| `listener_id` | number | AirLabs listener ID. |
| `performed` | string | Webhook performed date. |
| `res_headers` | object | Webhook response headers. |
| `res_status` | number | Webhook response status. |
| `webhook_id` | number | Webhook delivery ID. |
| `webhook_url` | string | Webhook destination URL. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /webhooks` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flight-alert-webhook-history.md) for the provider-specific parameters and requirements.

