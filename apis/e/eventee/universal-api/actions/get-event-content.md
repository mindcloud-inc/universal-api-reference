# Eventee: Get Event Content

Retrieves event content from Eventee.

```
GET https://connect.mindcloud.co/v1/universal/eventee/latest/actions/get-event-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventee/latest/actions/get-event-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventee/latest/actions/get-event-content?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "days": [
        {}
      ],
      "halls": [
        {}
      ],
      "lectures": [
        {}
      ],
      "pauses": [
        {}
      ],
      "speakers": [
        {}
      ],
      "tracks": [
        {}
      ],
      "workshops": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `days` | array<object> | Day objects returned by the content payload when present. |
| `halls` | array<object> | Hall objects included in the event content payload. |
| `lectures` | array<object> | Lecture session objects in the event content payload. |
| `pauses` | array<object> | Pause or break objects in the event content payload. |
| `speakers` | array<object> | Speaker objects included in the event content payload. |
| `tracks` | array<object> | Track objects included in the event content payload. |
| `workshops` | array<object> | Workshop session objects in the event content payload. |

## Native endpoint

Through the native Eventee API, this operation is `GET /content` (base URL `https://api.eventee.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-content.md) for the provider-specific parameters and requirements.

