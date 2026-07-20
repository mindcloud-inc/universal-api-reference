# Leap: Update Job Note

Updates an existing job note in Leap.

```
PUT https://connect.mindcloud.co/v1/universal/leap/latest/actions/update-job-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leap/latest/actions/update-job-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "note": "string",
  "noteId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leap/latest/actions/update-job-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "note": "string",
    "noteId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | string | yes | Updated text for the job note. |
| `noteId` | number | yes | Leap job note ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Updated note returned by Leap. |
| `message` | string | Provider success message. |
| `status` | number | HTTP-style status code returned by Leap. |

## Native endpoint

Through the native Leap API, this operation is `PUT /jobs/notes/[:noteId]` (base URL `https://api.jobprogress.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-job-note.md) for the provider-specific parameters and requirements.

