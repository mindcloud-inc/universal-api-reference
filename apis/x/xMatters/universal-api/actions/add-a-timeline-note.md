# xMatters: Add a timeline note

Adds a timeline note in your xMatters instance.

```
POST https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-timeline-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-timeline-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/add-a-timeline-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryType` | string | no |  |
| `incidentId` | string | no |  |
| `text` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedBy": {
        "firstName": "Ava",
        "id": "string",
        "lastName": "Chen",
        "links": {
          "self": "https://example.com"
        },
        "recipientType": "string",
        "status": "string",
        "targetName": "Ava Chen"
      },
      "at": "2026-05-07T12:00:00.000Z",
      "entryType": "string",
      "id": "string",
      "incident": {
        "id": "string",
        "links": {
          "self": "https://example.com"
        }
      },
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedBy.firstName` | string |  |
| `addedBy.id` | string |  |
| `addedBy.lastName` | string |  |
| `addedBy.links.self` | string |  |
| `addedBy.recipientType` | string |  |
| `addedBy.status` | string |  |
| `addedBy.targetName` | string |  |
| `at` | date |  |
| `entryType` | string |  |
| `id` | string |  |
| `incident.id` | string |  |
| `incident.links.self` | string |  |
| `text` | string |  |

## Native endpoint

Through the native xMatters API, this operation is `POST incidents/{incidentId}/timeline-entries` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-timeline-note.md) for the provider-specific parameters and requirements.

