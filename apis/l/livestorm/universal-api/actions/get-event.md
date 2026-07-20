# Livestorm: Get Event

Retrieves an event from Livestorm.

```
GET https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/get-event?${params}`, {
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
| `id` | string | yes | Event ID |
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

Through the native Livestorm API, this operation is `GET events/:id` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

