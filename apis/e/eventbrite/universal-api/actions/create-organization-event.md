# Eventbrite: Create Organization Event

Creates a new organization event in Eventbrite.

```
POST https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event.currency": "string",
  "event.end.timezone": "string",
  "event.end.utc": "string",
  "event.name.html": "Ava Chen",
  "event.start.timezone": "string",
  "event.start.utc": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/create-organization-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event.currency": "string",
    "event.end.timezone": "string",
    "event.end.utc": "string",
    "event.name.html": "Ava Chen",
    "event.start.timezone": "string",
    "event.start.utc": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event.currency` | string | yes | Event currency code (e.g. USD). |
| `event.end.timezone` | string | yes | End timezone (e.g. America/Chicago). |
| `event.end.utc` | string | yes | End datetime in UTC ISO format. |
| `event.name.html` | string | yes | Event title. |
| `event.start.timezone` | string | yes | Start timezone (e.g. America/Chicago). |
| `event.start.utc` | string | yes | Start datetime in UTC ISO format. |
| `organizationId` | string | yes | Organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capacity": 1,
      "capacityIsCustom": true,
      "categoryId": {},
      "changed": "string",
      "created": "string",
      "currency": "string",
      "description": {
        "html": {},
        "text": {}
      },
      "end": {
        "local": "string",
        "timezone": "string",
        "utc": "string"
      },
      "facebookEventId": {},
      "formatId": {},
      "hideEndDate": true,
      "hideStartDate": true,
      "id": "string",
      "inventoryType": "string",
      "inviteOnly": true,
      "isExternallyTicketed": true,
      "isFree": true,
      "isLocked": true,
      "isReservedSeating": true,
      "isSeries": true,
      "isSeriesParent": true,
      "listed": true,
      "locale": "string",
      "logo": {},
      "logoId": {},
      "name": {
        "html": "Ava Chen",
        "text": "Ava Chen"
      },
      "onlineEvent": true,
      "organizationId": "string",
      "organizerId": "string",
      "privacySetting": "string",
      "resourceUri": "string",
      "shareable": true,
      "showColorsInSeatmapThumbnail": true,
      "showPickASeat": true,
      "showRemaining": true,
      "showSeatmapThumbnail": true,
      "source": "string",
      "start": {
        "local": "string",
        "timezone": "string",
        "utc": "string"
      },
      "status": "string",
      "subcategoryId": {},
      "summary": {},
      "txTimeLimit": 1,
      "url": "https://example.com",
      "venueId": {},
      "version": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capacity` | number |  |
| `capacityIsCustom` | boolean |  |
| `categoryId` | object |  |
| `changed` | string |  |
| `created` | string |  |
| `currency` | string |  |
| `description.html` | object |  |
| `description.text` | object |  |
| `end.local` | string |  |
| `end.timezone` | string |  |
| `end.utc` | string |  |
| `facebookEventId` | object |  |
| `formatId` | object |  |
| `hideEndDate` | boolean |  |
| `hideStartDate` | boolean |  |
| `id` | string |  |
| `inventoryType` | string |  |
| `inviteOnly` | boolean |  |
| `isExternallyTicketed` | boolean |  |
| `isFree` | boolean |  |
| `isLocked` | boolean |  |
| `isReservedSeating` | boolean |  |
| `isSeries` | boolean |  |
| `isSeriesParent` | boolean |  |
| `listed` | boolean |  |
| `locale` | string |  |
| `logo` | object |  |
| `logoId` | object |  |
| `name.html` | string |  |
| `name.text` | string |  |
| `onlineEvent` | boolean |  |
| `organizationId` | string |  |
| `organizerId` | string |  |
| `privacySetting` | string |  |
| `resourceUri` | string |  |
| `shareable` | boolean |  |
| `showColorsInSeatmapThumbnail` | boolean |  |
| `showPickASeat` | boolean |  |
| `showRemaining` | boolean |  |
| `showSeatmapThumbnail` | boolean |  |
| `source` | string |  |
| `start.local` | string |  |
| `start.timezone` | string |  |
| `start.utc` | string |  |
| `status` | string |  |
| `subcategoryId` | object |  |
| `summary` | object |  |
| `txTimeLimit` | number |  |
| `url` | string |  |
| `venueId` | object |  |
| `version` | object |  |

## Native endpoint

Through the native Eventbrite API, this operation is `POST /organizations/:organizationId/events/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-organization-event.md) for the provider-specific parameters and requirements.

