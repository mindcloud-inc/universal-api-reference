# Lunatask: Create Person Timeline Note



```
POST https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-person-timeline-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lunatask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-person-timeline-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "personId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/create-person-timeline-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "personId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | string | yes | The Person ID of the person for the timeline note |
| `dateOn` | date | no | ISO-8601 formatted date for the timeline note |
| `content` | string | no | The content of the timeline note in Markdown |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dateOn": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "personId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `createdAt` | date |  |
| `dateOn` | date |  |
| `id` | string |  |
| `personId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Lunatask API, this operation is `POST /person_timeline_notes` (base URL `https://api.lunatask.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person-timeline-note.md) for the provider-specific parameters and requirements.

