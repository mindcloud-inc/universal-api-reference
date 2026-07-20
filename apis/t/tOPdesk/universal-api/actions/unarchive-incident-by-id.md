# TOPdesk: Unarchive Incident by ID

Unarchives an incident in TOPdesk by ID.

```
PUT https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/unarchive-incident-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TOPdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/unarchive-incident-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/unarchive-incident-by-id', {
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
| `id` | string | yes | Incident identifier. |
| `unarchivePartials` | boolean | no | Whether linked partial incidents should be unarchived as well. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "briefDescription": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "escalationStatus": "string",
      "id": "string",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "number": "string",
      "status": "string",
      "targetDate": "2026-05-07T12:00:00.000Z",
      "timeSpent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `briefDescription` | string |  |
| `creationDate` | date |  |
| `escalationStatus` | string |  |
| `id` | string |  |
| `modificationDate` | date |  |
| `number` | string |  |
| `status` | string |  |
| `targetDate` | date |  |
| `timeSpent` | number |  |

## Native endpoint

Through the native TOPdesk API, this operation is `PUT /incidents/id/:id/unarchive` (base URL `https://usatopdesktrial2.topdesk.net/tas/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unarchive-incident-by-id.md) for the provider-specific parameters and requirements.

