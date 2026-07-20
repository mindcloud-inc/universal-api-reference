# Nutshell: List Activities

Retrieves activities from Nutshell.

```
GET https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nutshell `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nutshell/latest/actions/list-activities?${params}`, {
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
| `q` | string | no | Search across activities. |
| `limit` | date | no | Maximum number of activities to return. |
| `filter.activityType[]` | array<number> | no | Filter activities by activity type. Accepts multiple values as an array. |
| `filter.status[]` | array<string> | no | Filter activities by status. Accepts multiple values as an array. |
| `filter.participant[]` | array<string> | no | Filter activities by participant. Accepts multiple values as an array. |
| `filter.flagged` | boolean | no | Filter to flagged or unflagged activities. |
| `filter.isImportant` | boolean | no | Filter to important or non-important activities. |
| `filter.leadPriority` | string | no | Filter activities by lead priority. |
| `filter.dateMin` | date | no | Return activities on or after this date. |
| `filter.dateMax` | date | no | Return activities on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agenda": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "deletedTime": {},
      "endTime": "2026-05-07T12:00:00.000Z",
      "externalMeetingServiceType": {},
      "href": "string",
      "htmlUrl": "https://example.com",
      "htmlUrlPath": "https://example.com",
      "id": "string",
      "isAllDay": true,
      "isCancelled": true,
      "isEditable": true,
      "isFlagged": true,
      "isLogged": true,
      "isMediaLogged": true,
      "isOverdue": true,
      "isPrivate": "string",
      "links": {
        "activityType": "https://example.com",
        "contacts": [
          "https://example.com"
        ],
        "creator": "https://example.com",
        "logger": {},
        "logNote": "https://example.com"
      },
      "loggedTime": "2026-05-07T12:00:00.000Z",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "showTranscribeLoggingFlow": true,
      "startTime": "2026-05-07T12:00:00.000Z",
      "transcription": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agenda` | string |  |
| `createdTime` | date |  |
| `deletedTime` | object |  |
| `endTime` | date |  |
| `externalMeetingServiceType` | object |  |
| `href` | string |  |
| `htmlUrl` | string |  |
| `htmlUrlPath` | string |  |
| `id` | string |  |
| `isAllDay` | boolean |  |
| `isCancelled` | boolean |  |
| `isEditable` | boolean |  |
| `isFlagged` | boolean |  |
| `isLogged` | boolean |  |
| `isMediaLogged` | boolean |  |
| `isOverdue` | boolean |  |
| `isPrivate` | string |  |
| `links.activityType` | string |  |
| `links.contacts[]` | string |  |
| `links.creator` | string |  |
| `links.logger` | object |  |
| `links.logNote` | string |  |
| `loggedTime` | date |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `showTranscribeLoggingFlow` | boolean |  |
| `startTime` | date |  |
| `transcription` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Nutshell API, this operation is `GET /activities` (base URL `https://app.nutshell.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-activities.md) for the provider-specific parameters and requirements.

