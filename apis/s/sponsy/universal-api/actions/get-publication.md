# Sponsy: Get Publication

Retrieves a publication from Sponsy.

```
GET https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-publication
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sponsy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-publication?connectionId=$CONNECTION_ID&publicationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "publicationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sponsy/latest/actions/get-publication?${params}`, {
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
| `publicationId` | list<string> | yes | Publication ID from List Publications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appleShowUrl": "https://example.com",
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "blockedDates": [
        "string"
      ],
      "categories": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorName": "Ava Chen",
      "days": [
        "string"
      ],
      "defaultDueDate": "2026-05-07T12:00:00.000Z",
      "hideBlockedDates": true,
      "id": "string",
      "name": "Ava Chen",
      "order": 1,
      "scheduleFrequency": "string",
      "scheduleFrequencyValue": 1,
      "scheduleReferenceDate": "2026-05-07T12:00:00.000Z",
      "scheduleReferenceTo": "string",
      "slug": "string",
      "spotifyShowUrl": "https://example.com",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appleShowUrl` | string | Apple show URL when configured. |
| `archivedAt` | date | Archive timestamp when present. |
| `blockedDates` | array<string> | Blocked publication dates. |
| `categories` | array<string> | Publication categories. |
| `createdAt` | date | Publication creation timestamp. |
| `creatorName` | string | Creator name when available. |
| `days` | array<string> | Scheduled publication weekdays. |
| `defaultDueDate` | date | Default due date when configured. |
| `hideBlockedDates` | boolean | Whether blocked dates are hidden in the calendar. |
| `id` | string | Sponsy publication ID. |
| `name` | string | Publication name. |
| `order` | number | Publication display order. |
| `scheduleFrequency` | string | Publication schedule cadence. |
| `scheduleFrequencyValue` | number | Publication schedule cadence interval value. |
| `scheduleReferenceDate` | date | Reference date for the publication schedule when present. |
| `scheduleReferenceTo` | string | Publication schedule reference type. |
| `slug` | string | Publication slug. |
| `spotifyShowUrl` | string | Spotify show URL when configured. |
| `type` | string | Publication type. |
| `updatedAt` | date | Publication update timestamp. |

## Native endpoint

Through the native Sponsy API, this operation is `GET /v1/publications/:publicationId` (base URL `https://api.getsponsy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-publication.md) for the provider-specific parameters and requirements.

