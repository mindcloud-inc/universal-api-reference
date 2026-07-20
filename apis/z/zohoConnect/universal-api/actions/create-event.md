# Zoho Connect: Create Event

Creates a new event in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "title": "string",
  "startYear": 1,
  "startMonth": 1,
  "startDate": 1,
  "startHour": 1,
  "startMin": 1,
  "endYear": 1,
  "endMonth": 1,
  "endDate": 1,
  "endHour": 1,
  "endMin": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "title": "string",
    "startYear": 1,
    "startMonth": 1,
    "startDate": 1,
    "startHour": 1,
    "startMin": 1,
    "endYear": 1,
    "endMonth": 1,
    "endDate": 1,
    "endHour": 1,
    "endMin": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes |  |
| `partitionId` | string | no | Optional partition context for the event. Defaults to the user's wall when omitted. |
| `title` | string | yes |  |
| `description` | string | no |  |
| `location` | string | no |  |
| `fields` | string | no | Comma-separated file IDs uploaded through Zoho's file upload API. Up to 10 files per event. Accepts multiple values in one string, delimited by `,`. |
| `startYear` | number | yes |  |
| `startMonth` | number | yes |  |
| `startDate` | number | yes |  |
| `startHour` | number | yes |  |
| `startMin` | number | yes |  |
| `endYear` | number | yes |  |
| `endMonth` | number | yes |  |
| `endDate` | number | yes |  |
| `endHour` | number | yes |  |
| `endMin` | number | yes |  |
| `allDay` | boolean | no |  |
| `intervalDay` | number | no |  |
| `intervalMinute` | number | no |  |
| `intervalHour` | number | no |  |
| `invitedMembers` | string | no | Accepts multiple values in one string, delimited by `,`. |
| `invitedGroups` | string | no | Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addEvent": {
        "stream": {
          "event": {
            "endTime": "string",
            "location": "string",
            "startTime": "string",
            "streamId": "string",
            "title": "string"
          },
          "id": "string",
          "link": {
            "linkurl": "https://example.com",
            "title": "https://example.com"
          },
          "status": "string",
          "type": "string",
          "url": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addEvent.stream.event.endTime` | string |  |
| `addEvent.stream.event.location` | string |  |
| `addEvent.stream.event.startTime` | string |  |
| `addEvent.stream.event.streamId` | string |  |
| `addEvent.stream.event.title` | string |  |
| `addEvent.stream.id` | string |  |
| `addEvent.stream.link.linkurl` | string |  |
| `addEvent.stream.link.title` | string |  |
| `addEvent.stream.status` | string |  |
| `addEvent.stream.type` | string |  |
| `addEvent.stream.url` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/addEvent` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

