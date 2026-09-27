# Get event attendees with ConnectSafely

Fetch the list of people who have RSVPed or are attending a LinkedIn event. Returns profile information for each attendee including name, headline, location, profile picture, and connection degree. Supports pagination (LinkedIn fixes page size at 10). Accepts a numeric event ID, a full LinkedIn event URL, or a search URL containing an `eventAttending` parameter.

## Endpoint

- **Method:** `GET`
- **Path:** `/events/:eventId/attendees`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get event attendees](https://connectsafely.ai/docs/api/uncategorized/get-events-eventid-attendees-get-event-attendees)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | param | `string` | yes | LinkedIn event ID (numeric), full event URL, or search URL with eventAttending parameter. |
| `accountId` | query | `string` | no | LinkedIn account ID. If omitted, uses the default account. |
| `start` | query | `number` | no | Pagination offset (0-indexed). Increment by 10 to paginate. Default: `0`. |
| `count` | query | `number` | no | Number of attendees to return per page (max 100, LinkedIn typically returns 10). Default: `10`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `eventId` | `string` | Resolved numeric event ID |
| `attendees` | `array` |  |
| `attendees[].profileUrn` | `string` | LinkedIn tracking URN for the profile |
| `attendees[].fsdProfileUrn` | `string` | FSD profile URN (e.g. urn:li:fsd_profile:ABCDE) |
| `attendees[].publicIdentifier` | `string` | Profile vanity slug (e.g. john-doe) |
| `attendees[].fullName` | `string` | Attendee full name |
| `attendees[].headline` | `string` | Professional headline |
| `attendees[].location` | `string` | Location from profile |
| `attendees[].profilePictureUrl` | `string` | URL of the profile picture |
| `attendees[].profileUrl` | `string` | Full LinkedIn profile URL |
| `attendees[].connectionDegree` | `string` | Connection degree (DISTANCE_1, DISTANCE_2, DISTANCE_3) |
| `paging` | `object` |  |
| `paging.start` | `number` | Current offset |
| `paging.count` | `number` | Requested page size |
| `paging.total` | `number` | Total number of attendees (may be absent) |

### Example response

```json
{
  "success": true,
  "accountId": "acc_12345",
  "eventId": "7453424948037070848",
  "attendees": [
    {
      "profileUrn": "urn:li:member:123456789",
      "fsdProfileUrn": "urn:li:fsd_profile:ABCDE",
      "publicIdentifier": "jane-doe",
      "fullName": "Jane Doe",
      "headline": "VP of Marketing at Acme Corp",
      "location": "San Francisco Bay Area",
      "profilePictureUrl": "https://media.licdn.com/dms/image/example.jpg",
      "profileUrl": "https://www.linkedin.com/in/jane-doe",
      "connectionDegree": "DISTANCE_2"
    }
  ],
  "paging": {
    "start": 0,
    "count": 10,
    "total": 142
  }
}
```

## Error status codes

`400`, `401`, `500`, `502`. Bodies follow the shared `{ success, code, message }` error shape.
