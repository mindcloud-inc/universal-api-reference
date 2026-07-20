# Routee: Retrieve Conversation dial Tracking

Retrieves conversation dial tracking from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-conversation-dial-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-conversation-dial-tracking?connectionId=$CONNECTION_ID&conversationTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-conversation-dial-tracking?${params}`, {
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
| `conversationTrackingId` | string | yes | The tracking id of the conversation which includes the dials. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        [
          {}
        ]
      ],
      "first": true,
      "last": true,
      "number": 1,
      "numberOfElements": 1,
      "size": 1,
      "totalElements": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content[]` | array<object> |  |
| `content[].chargeInterval` | number |  |
| `content[].conversationTrackingId` | string |  |
| `content[].country` | string |  |
| `content[].direction` | string |  |
| `content[].duration` | number |  |
| `content[].from` | string |  |
| `content[].messageId` | string |  |
| `content[].originatingService` | string |  |
| `content[].price` | number |  |
| `content[].recordings[]` | array |  |
| `content[].status` | object |  |
| `content[].status.date` | string |  |
| `content[].status.status` | string |  |
| `content[].to` | string |  |
| `first` | boolean |  |
| `last` | boolean |  |
| `number` | number |  |
| `numberOfElements` | number |  |
| `size` | number |  |
| `totalElements` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native Routee API, this operation is `GET /voice/tracking/conversation/:conversationTrackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-conversation-dial-tracking.md) for the provider-specific parameters and requirements.

