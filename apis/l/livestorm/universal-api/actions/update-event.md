# Livestorm: Update Event

Updates an existing event in Livestorm.

```
PUT https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/update-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Livestorm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/update-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/livestorm/latest/actions/update-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Event ID |
| `data.attributes.ownerId` | string | no |  |
| `data.attributes.title` | string | no |  |
| `data.attributes.slug` | string | no |  |
| `data.attributes.status` | string | no |  |
| `data.attributes.everyoneCanSpeak` | boolean | no |  |
| `data.attributes.detailedRegistrationPageEnabled` | boolean | no |  |
| `data.attributes.lightRegistrationPageEnabled` | boolean | no |  |
| `data.attributes.description` | string | no |  |
| `data.attributes.recordingEnabled` | boolean | no |  |
| `data.attributes.recordingPublic` | boolean | no |  |
| `data.attributes.showInCompanyPage` | boolean | no |  |
| `data.attributes.chatEnabled` | boolean | no |  |
| `data.attributes.questionsEnabled` | boolean | no |  |
| `data.attributes.pollsEnabled` | boolean | no |  |

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

Through the native Livestorm API, this operation is `PATCH events/:id` (base URL `https://api.livestorm.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-event.md) for the provider-specific parameters and requirements.

