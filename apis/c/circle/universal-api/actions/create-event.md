# Circle: Create Event

Creates a new event in Circle.

```
POST https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Circle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": {},
  "spaceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/circle/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": {},
    "spaceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | object | yes | Event payload object |
| `spaceId` | list<number> | yes | Space ID for the event |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "commentsCount": 1,
      "communityMemberId": 1,
      "confirmationMessageButtonLink": "https://example.com",
      "confirmationMessageButtonTitle": "string",
      "confirmationMessageDescription": "string",
      "confirmationMessageTitle": "string",
      "coverImageUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "durationInSeconds": 1,
      "enableCustomThankYouMessage": true,
      "endsAt": "2026-05-07T12:00:00.000Z",
      "hideAttendees": true,
      "hideLocationFromNonAttendees": true,
      "hideMetaInfo": "string",
      "host": "string",
      "id": 1,
      "inPersonLocation": "string",
      "likesCount": 1,
      "locationType": "string",
      "memberAvatarUrl": "https://example.com",
      "memberEmail": "ava@example.com",
      "memberName": "Ava Chen",
      "name": "Ava Chen",
      "rsvpDisabled": true,
      "sendEmailConfirmation": true,
      "sendEmailReminder": true,
      "sendInAppNotificationConfirmation": true,
      "sendInAppNotificationReminder": true,
      "slug": "string",
      "space": {
        "communityId": 1,
        "id": 1,
        "name": "Ava Chen",
        "slug": "string"
      },
      "startsAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "userId": 1,
      "virtualLocationUrl": "https://example.com",
      "zapierDisplayTitle": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `commentsCount` | number |  |
| `communityMemberId` | number |  |
| `confirmationMessageButtonLink` | string |  |
| `confirmationMessageButtonTitle` | string |  |
| `confirmationMessageDescription` | string |  |
| `confirmationMessageTitle` | string |  |
| `coverImageUrl` | string |  |
| `createdAt` | date |  |
| `durationInSeconds` | number |  |
| `enableCustomThankYouMessage` | boolean |  |
| `endsAt` | date |  |
| `hideAttendees` | boolean |  |
| `hideLocationFromNonAttendees` | boolean |  |
| `hideMetaInfo` | string |  |
| `host` | string |  |
| `id` | number |  |
| `inPersonLocation` | string |  |
| `likesCount` | number |  |
| `locationType` | string |  |
| `memberAvatarUrl` | string |  |
| `memberEmail` | string |  |
| `memberName` | string |  |
| `name` | string |  |
| `rsvpDisabled` | boolean |  |
| `sendEmailConfirmation` | boolean |  |
| `sendEmailReminder` | boolean |  |
| `sendInAppNotificationConfirmation` | boolean |  |
| `sendInAppNotificationReminder` | boolean |  |
| `slug` | string |  |
| `space.communityId` | number |  |
| `space.id` | number |  |
| `space.name` | string |  |
| `space.slug` | string |  |
| `startsAt` | date |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `userId` | number |  |
| `virtualLocationUrl` | string |  |
| `zapierDisplayTitle` | date |  |

## Native endpoint

Through the native Circle API, this operation is `POST /api/admin/v2/events` (base URL `https://{{credentials.subdomain}}.circle.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

