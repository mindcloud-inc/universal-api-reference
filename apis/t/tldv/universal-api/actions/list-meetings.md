# tl:dv: List Meetings

Retrieves meetings from tl:dv.

```
GET https://connect.mindcloud.co/v1/universal/tldv/latest/actions/list-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a tl:dv `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tldv/latest/actions/list-meetings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tldv/latest/actions/list-meetings?${params}`, {
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
| `query` | string | no | Search meetings by keyword. |
| `from` | date | no | Return meetings from this date forward. |
| `to` | date | no | Return meetings up to this date. |
| `onlyParticipated` | boolean | no | Only include meetings the authenticated user participated in. |
| `meetingType` | string | no | Filter meetings by type. |

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
| `url` | string | The meeting URL. |

## Native endpoint

Through the native tl:dv API, this operation is `GET /v1alpha1/meetings` (base URL `https://pasta.tldv.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-meetings.md) for the provider-specific parameters and requirements.

