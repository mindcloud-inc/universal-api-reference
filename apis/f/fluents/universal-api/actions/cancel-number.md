# Fluents: Cancel Number

Cancels an existing phone number from Fluents.

```
DELETE https://connect.mindcloud.co/v1/universal/fluents/latest/actions/cancel-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/cancel-number?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/cancel-number?${params}`, {
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
| `id` | string | yes | Fluents phone number ID to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "config": {},
      "description": "string",
      "example_context": {},
      "id": "string",
      "inbound_agent": {},
      "is_routing_number": true,
      "label": "string",
      "number": "string",
      "outbound_only": true,
      "sms_enabled": true,
      "tags": [
        "string"
      ],
      "telephony_account_connection": "string",
      "telephony_provider": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `config` | object |  |
| `description` | string |  |
| `example_context` | object |  |
| `id` | string |  |
| `inbound_agent` | object |  |
| `is_routing_number` | boolean |  |
| `label` | string |  |
| `number` | string |  |
| `outbound_only` | boolean |  |
| `sms_enabled` | boolean |  |
| `tags` | array<string> |  |
| `telephony_account_connection` | string |  |
| `telephony_provider` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /numbers/cancel` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-number.md) for the provider-specific parameters and requirements.

