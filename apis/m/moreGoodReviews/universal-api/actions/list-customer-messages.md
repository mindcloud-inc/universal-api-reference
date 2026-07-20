# More Good Reviews: List Customer Messages

Retrieves messages for a customer in More Good Reviews.

```
GET https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customer-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a More Good Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customer-messages?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moreGoodReviews/latest/actions/list-customer-messages?${params}`, {
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
| `id` | string | yes | The customer identifier. |

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
        "color": "string",
        "gravatar": "string",
        "id": 1,
        "name": "Ava Chen",
        "uuid": "string"
      },
      "id": 1,
      "scheduled_at": 1,
      "template": {
        "channel": "string",
        "id": 1,
        "name": "Ava Chen",
        "slug": "string",
        "uuid": "string"
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
| `customer.color` | string |  |
| `customer.gravatar` | string |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customer.uuid` | string |  |
| `id` | number |  |
| `scheduled_at` | number |  |
| `template.channel` | string |  |
| `template.id` | number |  |
| `template.name` | string |  |
| `template.slug` | string |  |
| `template.uuid` | string |  |
| `updated_at` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native More Good Reviews API, this operation is `GET /beacon/customers/:id/messages` (base URL `https://api.moregoodreviews.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-messages.md) for the provider-specific parameters and requirements.

