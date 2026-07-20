# AskHandle: Retrieve Webhook

Retrieves one AskHandle webhook by UUID.

```
GET https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/retrieve-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/retrieve-webhook?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/retrieve-webhook?${params}`, {
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
| `uuid` | string | no | The webhook UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event": "string",
      "target": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event` | string | Webhook event name. |
| `target` | string | Webhook target URL. |
| `uuid` | string | Webhook UUID. |

## Native endpoint

Through the native AskHandle API, this operation is `GET /webhooks/:uuid/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-webhook.md) for the provider-specific parameters and requirements.

