# Saastic: List Customer Messages

Retrieves messages for a customer from Saastic.

```
GET https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customer-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Saastic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customer-messages?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/saastic/latest/actions/list-customer-messages?${params}`, {
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
| `id` | string | yes | The customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ask_id": 1,
      "channel": "string",
      "created_at": 1,
      "customer": {
        "id": 1,
        "name": "Ava Chen"
      },
      "failed_at": 1,
      "id": 1,
      "scheduled_at": 1,
      "sent_at": 1,
      "template": {
        "channel": "string",
        "id": 1,
        "name": "Ava Chen"
      },
      "updated_at": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ask_id` | number |  |
| `channel` | string |  |
| `created_at` | number |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `failed_at` | number |  |
| `id` | number |  |
| `scheduled_at` | number |  |
| `sent_at` | number |  |
| `template.channel` | string |  |
| `template.id` | number |  |
| `template.name` | string |  |
| `updated_at` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native Saastic API, this operation is `GET /beacon/customers/:id/messages` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-messages.md) for the provider-specific parameters and requirements.

