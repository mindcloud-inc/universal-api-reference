# boomApp Connect: Retrieve Message Responses

Retrieves responses to outbound messages from boomApp Connect.

```
GET https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-message-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-message-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/retrieve-message-responses?${params}`, {
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
| `unique_identifier` | string | no | Return responses for outbound messages with this unique_identifier. |
| `custom_parameter` | string | no | Return responses for outbound messages with this custom_parameter. |
| `campaign_name` | string | no | Return responses for outbound messages with this campaign_name. |
| `transaction_id` | string | no | Return responses for this outbound transaction ID. |
| `ignore_previous` | boolean | no | Exclude previously retrieved responses. |
| `mark_as_read` | boolean | no | Mark retrieved responses as read. |
| `conversationId` | string | no | Return responses for a conversation thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "message": "string",
      "replies": {
        "campaignName": "Ava Chen",
        "conversationId": "string",
        "customParameter": "string",
        "from": "string",
        "isNew": true,
        "responseContent": "string",
        "responseDate": "string",
        "responseId": "string",
        "transactionDate": "string",
        "transactionId": "string"
      },
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean | Whether more pages are available. |
| `message` | string | Response message. |
| `replies` | array<object> | Message replies returned for outbound messages. |
| `replies.campaignName` | string | Campaign name. |
| `replies.conversationId` | string | Conversation thread ID. |
| `replies.customParameter` | string | Custom reference value. |
| `replies.from` | string | Sender number or address. |
| `replies.isNew` | boolean | Whether the response is new. |
| `replies.responseContent` | string | Reply content. |
| `replies.responseDate` | string | Response date. |
| `replies.responseId` | string | Response ID. |
| `replies.transactionDate` | string | Original transaction date. |
| `replies.transactionId` | string | Outbound transaction ID. |
| `status` | number | Response status code. |

## Native endpoint

Through the native boomApp Connect API, this operation is `GET /v1/get_responses` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-message-responses.md) for the provider-specific parameters and requirements.

