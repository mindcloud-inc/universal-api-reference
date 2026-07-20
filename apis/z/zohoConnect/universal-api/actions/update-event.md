# Zoho Connect: Update Event

Updates an existing event in Zoho Connect.

```
PUT https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "streamId": "string",
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "streamId": "string",
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
| `streamId` | string | yes |  |
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
| `invitedGroups` | string | no | Groups to be invited to the event. Separate multiple groups by a comma. Accepts multiple values in one string, delimited by `,`. |
| `deleteMemInvitees` | string | no | Removed invitees. Separate multiple members by a comma. Accepts multiple values in one string, delimited by `,`. |
| `deleteGrpInvitees` | string | no | Removed groups that are invited. Separate multiple groups by a comma. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateEvent": {
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
| `updateEvent.stream.event.endTime` | string |  |
| `updateEvent.stream.event.location` | string |  |
| `updateEvent.stream.event.startTime` | string |  |
| `updateEvent.stream.event.streamId` | string |  |
| `updateEvent.stream.event.title` | string |  |
| `updateEvent.stream.id` | string |  |
| `updateEvent.stream.link.linkurl` | string |  |
| `updateEvent.stream.link.title` | string |  |
| `updateEvent.stream.status` | string |  |
| `updateEvent.stream.type` | string |  |
| `updateEvent.stream.url` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/updateEvent` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

