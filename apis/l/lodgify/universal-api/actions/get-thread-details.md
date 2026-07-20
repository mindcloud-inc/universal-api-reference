# Lodgify: Get Thread Details

Retrieves message thread details from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-thread-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-thread-details?connectionId=$CONNECTION_ID&threadUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/get-thread-details?${params}`, {
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
| `threadUid` | string | yes | Reservation thread UID from the booking details. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": {},
      "errorTitle": {},
      "guestEmail": "ava@example.com",
      "guestName": "Ava Chen",
      "isClosed": true,
      "isRead": true,
      "lastMessageDate": "string",
      "messages": [
        [
          "string"
        ]
      ],
      "threadUid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | object |  |
| `errorTitle` | object |  |
| `guestEmail` | string |  |
| `guestName` | string |  |
| `isClosed` | boolean |  |
| `isRead` | boolean |  |
| `lastMessageDate` | string |  |
| `messages[]` | array<string> |  |
| `threadUid` | string |  |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v2/messaging/:threadUid` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread-details.md) for the provider-specific parameters and requirements.

