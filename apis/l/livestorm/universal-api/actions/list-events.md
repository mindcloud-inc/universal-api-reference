# Livestorm: List Events

Retrieves events from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/list-events?${params}`, {
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
| `filter[title]` | string | no | Filter Events by title |
| `filter[everyoneCanSpeak]` | string | no | Filter Events by everyone_can_speak |
| `filter[schedulingStatus]` | string | no | Filter Events by scheduling_status (live, upcoming, on_demand, ended, not_started, draft, cancelled, not_scheduled) |
| `filter[createdSince]` | date | no | Filter Events which ‘created_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[createdUntil]` | date | no | Filter Events which ‘created_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updatedSince]` | date | no | Filter Events which ‘updated_at’ attribute starts from the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[updatedUntil]` | date | no | Filter Events which ‘updated_at’ attribute ends with the given date (expressed as a Unix timestamp or an ISO 8601 date). |
| `filter[tag]` | string | no | Filter Events by tag title (case-insensitive, comma-separated for multiple tags) Accepts multiple values in one string, delimited by `,`. |
| `include` | string | no | Include Related Data Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "chatEnabled": true,
        "createdAt": 1,
        "description": "string",
        "detailedRegistrationPageEnabled": true,
        "estimatedDuration": 1,
        "everyoneCanSpeak": true,
        "fields": [
          [
            {}
          ]
        ],
        "language": "string",
        "lightRegistrationPageEnabled": true,
        "pollsEnabled": true,
        "publishedAt": 1,
        "questionsEnabled": true,
        "recordingEnabled": true,
        "recordingPublic": true,
        "registrationLink": "https://example.com",
        "registrationPageEnabled": true,
        "sessionsCount": 1,
        "showInCompanyPage": true,
        "slug": "string",
        "status": "string",
        "title": "string",
        "updatedAt": 1
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.chatEnabled` | boolean |  |
| `attributes.createdAt` | number |  |
| `attributes.description` | string |  |
| `attributes.detailedRegistrationPageEnabled` | boolean |  |
| `attributes.estimatedDuration` | number |  |
| `attributes.everyoneCanSpeak` | boolean |  |
| `attributes.fields[]` | array<object> |  |
| `attributes.fields[].id` | string |  |
| `attributes.fields[].order` | number |  |
| `attributes.fields[].required` | boolean |  |
| `attributes.fields[].type` | string |  |
| `attributes.language` | string |  |
| `attributes.lightRegistrationPageEnabled` | boolean |  |
| `attributes.pollsEnabled` | boolean |  |
| `attributes.publishedAt` | number |  |
| `attributes.questionsEnabled` | boolean |  |
| `attributes.recordingEnabled` | boolean |  |
| `attributes.recordingPublic` | boolean |  |
| `attributes.registrationLink` | string |  |
| `attributes.registrationPageEnabled` | boolean |  |
| `attributes.sessionsCount` | number |  |
| `attributes.showInCompanyPage` | boolean |  |
| `attributes.slug` | string |  |
| `attributes.status` | string |  |
| `attributes.title` | string |  |
| `attributes.updatedAt` | number |  |
| `id` | string | ID |
| `type` | string | Type |

## Native endpoint

Through the native Livestorm API, this operation is `GET events` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

