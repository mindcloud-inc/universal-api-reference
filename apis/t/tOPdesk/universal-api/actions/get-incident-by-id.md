# TOPdesk: Get Incident by ID

Retrieves an incident from TOPdesk by ID.

```
GET https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/get-incident-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TOPdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/get-incident-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/get-incident-by-id?${params}`, {
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
| `id` | string | yes | Incident identifier. |

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

Through the native TOPdesk API, this operation is `GET /incidents/id/:id` (base URL `https://usatopdesktrial2.topdesk.net/tas/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-incident-by-id.md) for the provider-specific parameters and requirements.

