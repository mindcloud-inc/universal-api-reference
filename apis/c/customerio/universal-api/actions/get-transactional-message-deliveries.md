# Customer.io: Get Transactional Message Deliveries

Retrieves deliveries for a Customer.io transactional message.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message-deliveries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message-deliveries?connectionId=$CONNECTION_ID&transactionalId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionalId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message-deliveries?${params}`, {
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
| `transactionalId` | number | yes | The identifier of your transactional message. Example: `3`. |
| `limit` | number | no | The maximum number of results you want to retrieve per page. Example: `100`. |
| `metric` | list<string> | no | Determines the metric you want to return. One of: `attempted`, `bounced`, `clicked`, `converted`, `delivered`, `dropped`, `failed`, `opened`, `sent`, `spammed`, `undeliverable`, `unsubscribed`. Example: `delivered`. |
| `state` | list<string> | no | The state of the delivery set you want to return. One of: `attempted`, `drafted`, `failed`, `sent`. Example: `sent`. |
| `startTs` | number | no | The beginning timestamp for your query. Example: `1772820000`. |
| `endTs` | number | no | The ending timestamp for your query. Example: `1772823600`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | string | no | The token for the page of results you want to return. Example: `next-page-token`. |

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
      "customerIdentifiers": {},
      "deduplicateId": "string",
      "failureMessage": "string",
      "forgotten": true,
      "id": "string",
      "messageTemplateId": 1,
      "metrics": {},
      "newsletterId": 1,
      "parentActionId": 1,
      "recipient": "string",
      "subject": "string",
      "triggerEventId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | number | The action identifier associated with the delivery. |
| `broadcastId` | number | The broadcast identifier associated with the delivery. |
| `campaignId` | number | The campaign identifier associated with the delivery. |
| `contentId` | number | The content identifier associated with the delivery. |
| `created` | number | Unix timestamp when the delivery record was created. |
| `customerId` | string | The customer identifier associated with the delivery. |
| `customerIdentifiers` | object | The customer identifiers returned with the delivery. |
| `deduplicateId` | string | The Customer.io deduplication identifier for the delivery. |
| `failureMessage` | string | Failure details when the delivery failed. |
| `forgotten` | boolean | Whether the delivery has been forgotten by retention rules. |
| `id` | string | The delivery identifier. |
| `messageTemplateId` | number | The transactional message template identifier. |
| `metrics` | object | Delivery metrics returned for the message. |
| `newsletterId` | number | The newsletter identifier associated with the delivery. |
| `parentActionId` | number | The parent action identifier associated with the delivery. |
| `recipient` | string | The recipient for the delivery. |
| `subject` | string | The delivery subject line. |
| `triggerEventId` | string | The triggering event identifier for the delivery. |
| `type` | string | The delivery type. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/transactional/:transactional_id/messages` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transactional-message-deliveries.md) for the provider-specific parameters and requirements.

