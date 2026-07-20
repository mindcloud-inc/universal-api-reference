# AskHandle: Update Webhook Field

Updates one AskHandle webhook field by UUID.

```
PUT https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/update-webhook-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AskHandle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/update-webhook-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/askhandle/latest/actions/update-webhook-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "target": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | no | The webhook UUID. |
| `event` | string | yes | Webhook event name. |
| `target` | string | yes | Webhook target URL. |

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

Through the native AskHandle API, this operation is `PATCH /webhooks/:uuid/` (base URL `https://dashboard.askhandle.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook-field.md) for the provider-specific parameters and requirements.

