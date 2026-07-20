# VSCO Workspace: Create Event

Creates a new event in VSCO Workspace.

```
POST https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VSCO Workspace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allDay` | boolean | no |  |
| `channel` | string | no |  |
| `confirmed` | boolean | no |  |
| `descriptionHtml` | string | no |  |
| `endDate` | date | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `endTime` | string | no | A time string using 24-hour format (seconds are ignored) |
| `endUtc` | object | no |  |
| `galleryId` | string | no | A ULID entity identifier that is nullable. |
| `jobId` | string | no | A ULID entity identifier that is nullable. |
| `location` | object | no |  |
| `name` | string | no |  |
| `phoneNumber` | object | no |  |
| `startDate` | date | no | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `startTime` | string | no | A time string using 24-hour format (seconds are ignored) |
| `startUtc` | object | no |  |
| `timezoneName` | string | no | A VSCO Workspace approved timezone name. If `timezoneId` is provided then this will be ignored. |
| `timezoneId` | string | no | A ULID entity identifier that is nullable. |
| `typeId` | string | no | A ULID entity identifier that is nullable. |
| `virtualUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allDay": true,
      "channel": "string",
      "confirmed": true,
      "created": "2026-05-07T12:00:00.000Z",
      "descriptionHtml": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "endTime": "string",
      "endUtc": {},
      "externalMappings": [
        {}
      ],
      "galleryId": "string",
      "hidden": true,
      "id": "string",
      "jobId": "string",
      "location": {},
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phoneNumber": {},
      "readOnly": true,
      "startDate": "2026-05-07T12:00:00.000Z",
      "startTime": "string",
      "startUtc": {},
      "timezoneId": "string",
      "timezoneName": "Ava Chen",
      "typeId": "string",
      "virtualUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allDay` | boolean |  |
| `channel` | string |  |
| `confirmed` | boolean |  |
| `created` | date | A server timestamp (always in UTC) |
| `descriptionHtml` | string |  |
| `endDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `endTime` | string | A time string using 24-hour format (seconds are ignored) |
| `endUtc` | object |  |
| `externalMappings` | array<object> |  |
| `galleryId` | string | A ULID entity identifier that is nullable. |
| `hidden` | boolean | Whether or not the object is hidden. |
| `id` | string | A lowercase [ULID](https://github.com/ulid/spec) entity identifier |
| `jobId` | string | A ULID entity identifier that is nullable. |
| `location` | object |  |
| `modified` | date | A server timestamp (always in UTC) |
| `name` | string |  |
| `phoneNumber` | object |  |
| `readOnly` | boolean |  |
| `startDate` | date | A date string consisting of year, month and day in the timezone of the event if specified or the studio. |
| `startTime` | string | A time string using 24-hour format (seconds are ignored) |
| `startUtc` | object |  |
| `timezoneId` | string | A ULID entity identifier that is nullable. |
| `timezoneName` | string | A VSCO Workspace approved timezone name. If `timezoneId` is provided then this will be ignored. |
| `typeId` | string | A ULID entity identifier that is nullable. |
| `virtualUrl` | string |  |

## Native endpoint

Through the native VSCO Workspace API, this operation is `POST /event` (base URL `https://workspace.vsco.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

