# Customer.io: List Customer Messages

Retrieves messages sent to a customer in Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=customer_id_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerId": "customer_id_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-customer-messages?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startTs` | date | no | The beginning timestamp for the query. Example: `2026-01-01T00:00:00Z`. |
| `endTs` | date | no | The ending timestamp for the query. Example: `2026-01-31T23:59:59Z`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": 1,
      "broadcastId": 1,
      "campaignId": 1,
      "contentId": 1,
      "created": 1,
      "customerId": "string",
      "deduplicateId": "string",
      "failureMessage": "string",
      "forgotten": true,
      "id": "string",
      "metrics": {},
      "msgTemplateId": "string",
      "newsletterId": 1,
      "recipient": "string",
      "subject": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | number | The campaign action identifier associated with the message. |
| `broadcastId` | number | The broadcast identifier associated with the message. |
| `campaignId` | number | The campaign identifier associated with the message. |
| `contentId` | number | The content identifier associated with the message. |
| `created` | number | Unix timestamp when the message record was created. |
| `customerId` | string | The customer identifier associated with the message. |
| `deduplicateId` | string | The Customer.io deduplication identifier for the message. |
| `failureMessage` | string | Failure details when the message could not be delivered. |
| `forgotten` | boolean | Whether the message has been forgotten by retention rules. |
| `id` | string | The message identifier. |
| `metrics` | object | Delivery metrics returned for the message. |
| `msgTemplateId` | string | The template identifier for the message. |
| `newsletterId` | number | The newsletter identifier associated with the message. |
| `recipient` | string | The recipient address for the message. |
| `subject` | string | The message subject line. |
| `type` | string | The message type. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/customers/:customer_id/messages` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-messages.md) for the provider-specific parameters and requirements.

