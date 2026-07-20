# Agile CRM: Create Note

Creates a new note in Agile CRM.

```
POST https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agile CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_ids[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agileCRM/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_ids[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_ids[]` | array<number> | yes | Contact IDs for the note. Must be an array. |
| `subject` | string | no | Short note subject. Example: `Follow-up call notes`. |
| `description` | string | no | Note body content. Example: `Discussed implementation timeline and next steps.`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactIds": [
        "string"
      ],
      "contacts": [
        {
          "id": 1,
          "properties": [
            {
              "name": "Ava Chen",
              "type": "string",
              "value": "string"
            }
          ],
          "type": "string"
        }
      ],
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domainOwner": {
        "calendarUrl": "https://example.com",
        "calendarURL": "https://example.com",
        "domain": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "pic": "string",
        "scheduleId": "string"
      },
      "entityType": "string",
      "id": 1,
      "ownerId": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactIds[]` | string |  |
| `contacts[].id` | number |  |
| `contacts[].properties[].name` | string |  |
| `contacts[].properties[].type` | string |  |
| `contacts[].properties[].value` | string |  |
| `contacts[].type` | string |  |
| `createdTime` | date |  |
| `description` | string |  |
| `domainOwner.calendarUrl` | string |  |
| `domainOwner.calendarURL` | string |  |
| `domainOwner.domain` | string |  |
| `domainOwner.email` | string |  |
| `domainOwner.id` | number |  |
| `domainOwner.name` | string |  |
| `domainOwner.phone` | string |  |
| `domainOwner.pic` | string |  |
| `domainOwner.scheduleId` | string |  |
| `entityType` | string |  |
| `id` | number |  |
| `ownerId` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native Agile CRM API, this operation is `POST /notes` (base URL `https://mindcloud.agilecrm.com/dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

