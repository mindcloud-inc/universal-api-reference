# tl:dv: Get Meeting

Retrieves a meeting from tl:dv.

```
GET https://connect.mindcloud.co/v1/universal/tldv/latest/actions/get-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a tl:dv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/get-meeting?connectionId=$CONNECTION_ID&meetingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tldv/latest/actions/get-meeting?${params}`, {
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
| `meetingId` | string | yes | The tl:dv meeting identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "extraProperties": {},
      "happenedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invitees": [
        {}
      ],
      "name": "Ava Chen",
      "organizer": {},
      "template": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number | The meeting duration in seconds. |
| `extraProperties` | object | Additional meeting metadata such as conferenceId. |
| `happenedAt` | date | When the meeting happened. |
| `id` | string | The tl;dv meeting identifier. |
| `invitees` | array<object> | The meeting invitees. |
| `name` | string | The meeting name. |
| `organizer` | object | The meeting organizer. |
| `template` | object | The meeting template metadata. |
| `url` | string | The meeting URL. |

## Native endpoint

Through the native tl:dv API, this operation is `GET /v1alpha1/meetings/:meetingId` (base URL `https://pasta.tldv.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting.md) for the provider-specific parameters and requirements.

