# Customer.io: Get Transactional Message

Retrieves a transactional message from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message?connectionId=$CONNECTION_ID&transactionalId=3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionalId": "3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/get-transactional-message?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "hideMessageBody": true,
      "id": 1,
      "linkTracking": true,
      "name": "Ava Chen",
      "openTracking": true,
      "queueDrafts": true,
      "sendToUnsubscribed": true,
      "triggerName": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the transactional message was created. |
| `description` | string | The transactional message description. |
| `hideMessageBody` | boolean | Whether message contents are retained in delivery history. |
| `id` | number | The identifier Customer.io assigned to the transactional message. |
| `linkTracking` | boolean | Whether link tracking is enabled. |
| `name` | string | The transactional message name. |
| `openTracking` | boolean | Whether open tracking is enabled. |
| `queueDrafts` | boolean | Whether deliveries queue as drafts instead of sending automatically. |
| `sendToUnsubscribed` | boolean | Whether unsubscribed people can still trigger the message. |
| `triggerName` | string | The trigger name configured for the transactional message. |
| `updatedAt` | date | When the transactional message was last updated. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/transactional/:transactional_id` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transactional-message.md) for the provider-specific parameters and requirements.

