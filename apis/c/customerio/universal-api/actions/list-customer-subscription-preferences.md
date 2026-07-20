# Customer.io: List Customer Subscription Preferences

Retrieves subscription preferences for a customer in Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-subscription-preferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-subscription-preferences?connectionId=$CONNECTION_ID&customerId=customer_id_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "customer_id_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-subscription-preferences?${params}`, {
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
| `customerId` | string | yes | The ID of the customer to inspect. Example: `customer_id_123`. |
| `idType` | list<string> | no | The type of identifier provided in Customer ID. One of: `cio_id`, `email`, `id`. Example: `id`. |
| `language` | string | no | The language tag to use for translated subscription-center content. Example: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "header": {},
      "id": "string",
      "identifiers": {},
      "topics": [
        {}
      ],
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `header` | object | The subscription preference header content. |
| `id` | string | The customer identifier. |
| `identifiers` | object | The customer identifier map returned by Customer.io. |
| `topics` | array<object> | Topic-level subscription preferences for the customer. |
| `unsubscribed` | boolean | Whether the customer is globally unsubscribed. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/customers/:customer_id/subscription_preferences` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-subscription-preferences.md) for the provider-specific parameters and requirements.

