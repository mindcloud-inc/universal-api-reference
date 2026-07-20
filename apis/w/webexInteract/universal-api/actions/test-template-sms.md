# Webex Interact: Test template SMS

Tests a template SMS in Webex Interact.

```
POST https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/test-template-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex Interact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/test-template-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "template_id": "string",
  "to": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webexInteract/latest/actions/test-template-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "template_id": "string",
    "to": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Sender ID for the SMS message. Sender names must already exist in Webex Interact. |
| `global_merge_fields` | object | no | Global merge fields applied to all recipients unless overridden per recipient. |
| `name` | string | no | External request name returned in webhooks. |
| `skip_optout_check` | boolean | no | Bypass opt-out checks when true. |
| `template_id` | string | yes | Template ID from Webex Interact. Required for template SMS validation. |
| `to` | list<object> | yes | Array of destination objects containing recipient phone arrays and optional merge fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "messages": [
        {}
      ],
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Per-recipient validation errors. |
| `messages` | array<object> | Message validation results. |
| `request_id` | string | SMS API request ID. |

## Native endpoint

Through the native Webex Interact API, this operation is `POST /v1/sms/test` (base URL `https://api.webexinteract.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-template-sms.md) for the provider-specific parameters and requirements.

