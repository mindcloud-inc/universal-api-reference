# Eventbrite: List Venue Events

Retrieves venue events from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-venue-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-venue-events?connectionId=$CONNECTION_ID&venueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "venueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-venue-events?${params}`, {
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
| `venueId` | string | yes | Venue identifier. |

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
        "html": "string",
        "text": "string"
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
      "summary": "string",
      "txTimeLimit": 1,
      "url": "https://example.com",
      "venueId": "string",
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
| `description.html` | string |  |
| `description.text` | string |  |
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
| `summary` | string |  |
| `txTimeLimit` | number |  |
| `url` | string |  |
| `venueId` | string |  |
| `version` | object |  |

## Native endpoint

Through the native Eventbrite API, this operation is `GET /venues/:venueId/events/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-venue-events.md) for the provider-specific parameters and requirements.

