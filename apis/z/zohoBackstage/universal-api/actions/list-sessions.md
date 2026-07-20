# Zoho Backstage: List Sessions



```
GET https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Backstage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-sessions?connectionId=$CONNECTION_ID&portalId=string&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBackstage/latest/actions/list-sessions?${params}`, {
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
| `portalId` | string | yes | The Zoho Backstage portal ID. |
| `eventId` | string | yes | The Zoho Backstage event ID. |
| `day` | number | no | Return only sessions for a specific event day. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda": "string",
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "duration": 1,
      "featured": true,
      "hidden": true,
      "id": "string",
      "language": "string",
      "lastModifiedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string"
      },
      "lastModifiedTime": "2026-05-07T12:00:00.000Z",
      "sessionType": "string",
      "speakers": [
        {
          "addedOn": "2026-05-07T12:00:00.000Z",
          "alternateTelephone": "string",
          "company": "string",
          "country": "string",
          "description": "string",
          "designation": "string",
          "email": "ava@example.com",
          "facebook": "string",
          "featured": true,
          "firstName": "Ava",
          "id": "string",
          "instagram": "string",
          "joinedOn": "2026-05-07T12:00:00.000Z",
          "lastName": "Chen",
          "linkedin": "https://example.com",
          "medium": "string",
          "skills": "string",
          "status": 1,
          "statusString": "string",
          "telegram": "string",
          "telephone": "string",
          "twitter": "string"
        }
      ],
      "speakerToBeAnnounced": true,
      "startTime": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "track": "string",
      "venue": "string",
      "venueToBeAnnounced": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.id` | string |  |
| `createdTime` | date |  |
| `description` | string |  |
| `duration` | number |  |
| `featured` | boolean |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `language` | string |  |
| `lastModifiedBy.email` | string |  |
| `lastModifiedBy.firstName` | string |  |
| `lastModifiedBy.id` | string |  |
| `lastModifiedTime` | date |  |
| `sessionType` | string |  |
| `speakers[].addedOn` | date |  |
| `speakers[].alternateTelephone` | string |  |
| `speakers[].company` | string |  |
| `speakers[].country` | string |  |
| `speakers[].description` | string |  |
| `speakers[].designation` | string |  |
| `speakers[].email` | string |  |
| `speakers[].facebook` | string |  |
| `speakers[].featured` | boolean |  |
| `speakers[].firstName` | string |  |
| `speakers[].id` | string |  |
| `speakers[].instagram` | string |  |
| `speakers[].joinedOn` | date |  |
| `speakers[].lastName` | string |  |
| `speakers[].linkedin` | string |  |
| `speakers[].medium` | string |  |
| `speakers[].skills` | string |  |
| `speakers[].status` | number |  |
| `speakers[].statusString` | string |  |
| `speakers[].telegram` | string |  |
| `speakers[].telephone` | string |  |
| `speakers[].twitter` | string |  |
| `speakerToBeAnnounced` | boolean |  |
| `startTime` | date |  |
| `title` | string |  |
| `track` | string |  |
| `venue` | string |  |
| `venueToBeAnnounced` | boolean |  |

## Native endpoint

Through the native Zoho Backstage API, this operation is `GET /v3/portals/:portal_id/events/:event_id/sessions` (base URL `https://zohoapis.com/backstage`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

