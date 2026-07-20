# Belong: Get Event

Retrieves an event from Belong by ID or slug.

```
GET https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Belong `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-event?connectionId=$CONNECTION_ID&id=69d509a56e0cc96c27ed7e90" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "69d509a56e0cc96c27ed7e90"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-event?${params}`, {
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
| `id` | string | yes | Example: `69d509a56e0cc96c27ed7e90`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowMultiPass": true,
      "analytics": {},
      "category": [
        "string"
      ],
      "categoryParentID": {},
      "categorySubEventIDs": [
        {}
      ],
      "cost": 1,
      "costCurrency": "string",
      "coupons": [
        {}
      ],
      "coverImage": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "description": "string",
      "end": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "friendsInTrip": [
        {}
      ],
      "games": [
        {}
      ],
      "gasless": true,
      "geoRestrictedMinting": true,
      "googleId": {},
      "id": "string",
      "inputVoice": true,
      "isHidden": true,
      "link": "https://example.com",
      "locale": {},
      "localizations": [
        {}
      ],
      "location": {},
      "media": [
        {}
      ],
      "members": [
        {}
      ],
      "moderators": [
        {}
      ],
      "name": "Ava Chen",
      "online": true,
      "owner": "string",
      "paperServiceAllowed": true,
      "passStrategy": "string",
      "place": {},
      "private": true,
      "recurrence": {},
      "recurrenceParentId": {},
      "shareurlIDs": [
        {}
      ],
      "slug": {},
      "source": "string",
      "sourcePlatform": {},
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "timelineType": "string",
      "timezone": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibleToGroups": [
        {}
      ],
      "visibleToProperties": [
        {}
      ],
      "visibleToUsers": [
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
| `allowMultiPass` | boolean | Whether multiple passes are allowed. |
| `analytics` | object |  |
| `category` | array<string> | Event category labels. |
| `categoryParentID` | object |  |
| `categorySubEventIDs[]` | object |  |
| `cost` | number | Ticket or participation cost when present. |
| `costCurrency` | string | Currency code for the event cost. |
| `coupons[]` | object |  |
| `coverImage` | object |  |
| `createdAt` | date | Creation timestamp. |
| `customFields` | object |  |
| `description` | string | Event description. |
| `end` | date | Event end timestamp. |
| `eventType` | string | Belong event type identifier. |
| `friendsInTrip[]` | object |  |
| `games[]` | object |  |
| `gasless` | boolean | Whether gasless flows are enabled. |
| `geoRestrictedMinting` | boolean |  |
| `googleId` | object |  |
| `id` | string | Belong event ID. |
| `inputVoice` | boolean |  |
| `isHidden` | boolean | Whether the event is hidden from normal visibility. |
| `link` | string | External event link. |
| `locale` | object |  |
| `localizations[]` | object |  |
| `location` | object |  |
| `media` | array<object> | Media assets attached to the event. |
| `members[]` | object |  |
| `moderators[]` | object |  |
| `name` | string | Event title. |
| `online` | boolean | Whether the event is online. |
| `owner` | string | Owner user ID. |
| `paperServiceAllowed` | boolean | Whether paper service is allowed. |
| `passStrategy` | string | Pass issuance strategy when configured. |
| `place` | object | Venue or location details for the event. |
| `private` | boolean | Whether the event is private. |
| `recurrence` | object |  |
| `recurrenceParentId` | object |  |
| `shareurlIDs[]` | object |  |
| `slug` | object |  |
| `source` | string | System that created the event. |
| `sourcePlatform` | object |  |
| `start` | date | Event start timestamp. |
| `status` | string | Publication status for the event. |
| `timelineType` | string | Timeline classification used by Belong. |
| `timezone` | string | Timezone for the event schedule. |
| `updatedAt` | date | Last update timestamp. |
| `visibleToGroups[]` | object |  |
| `visibleToProperties[]` | object |  |
| `visibleToUsers[]` | object |  |

## Native endpoint

Through the native Belong API, this operation is `GET /events/:id` (base URL `https://api.belong.net/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

