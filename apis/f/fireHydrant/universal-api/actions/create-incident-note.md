# FireHydrant: Create Incident Note

Creates a new incident note in FireHydrant.

```
POST https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/create-incident-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/create-incident-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "incidentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/create-incident-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "incidentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | The incident note body. |
| `incidentId` | string | yes | The FireHydrant incident ID. |
| `occurredAt` | date | no | ISO8601 timestamp for when the note occurred. |
| `visibility` | list | no | Who can see the note. One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "conversations": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "statusPages": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `conversations` | array<object> |  |
| `createdAt` | date |  |
| `id` | string |  |
| `statusPages` | array<object> |  |

## Native endpoint

Through the native FireHydrant API, this operation is `POST /incidents/:incident_id/notes` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident-note.md) for the provider-specific parameters and requirements.

