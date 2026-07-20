# Lemcal: List Booked Meetings

Retrieves your booked meetings from Lemcal.

```
GET https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/list-booked-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lemcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/list-booked-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/list-booked-meetings?${params}`, {
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
| `meetingTypeId` | string | no | Filter meetings by a specific meeting type ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "attendees": [
        {}
      ],
      "attendeeTimezone": "string",
      "createdAt": "string",
      "end": "string",
      "eventId": "string",
      "leadId": "string",
      "meetingTypeId": "string",
      "providedInfos": "string",
      "start": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `attendees` | array<object> |  |
| `attendeeTimezone` | string |  |
| `createdAt` | string |  |
| `end` | string |  |
| `eventId` | string |  |
| `leadId` | string |  |
| `meetingTypeId` | string |  |
| `providedInfos` | string |  |
| `start` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Lemcal API, this operation is `GET /meetings` (base URL `https://api.lemcal.com/api/lemcal`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-booked-meetings.md) for the provider-specific parameters and requirements.

