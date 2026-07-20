# Routee: Retrieve Conversation by TrackingId

Retrieves conversation by tracking ID from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-conversation-by-trackingid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-conversation-by-trackingid?connectionId=$CONNECTION_ID&conversationTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-conversation-by-trackingid?${params}`, {
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
| `conversationTrackingId` | string | yes | The tracking id of the conversation which includes the dialPlan. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "direction": "string",
      "from": "string",
      "recordings": [
        [
          {}
        ]
      ],
      "to": {
        "phone": "string"
      },
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `recordings[]` | array<object> |  |
| `recordings[].conversationTrackingId` | string |  |
| `recordings[].duration` | number |  |
| `recordings[].end` | string |  |
| `recordings[].from` | string |  |
| `recordings[].start` | string |  |
| `recordings[].to` | string |  |
| `recordings[].trackingId` | string |  |
| `recordings[].url` | string |  |
| `recordings[].voiceTrackingIds[]` | array<string> |  |
| `to` | object |  |
| `to.phone` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /voice/conversation/:conversationTrackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-conversation-by-trackingid.md) for the provider-specific parameters and requirements.

