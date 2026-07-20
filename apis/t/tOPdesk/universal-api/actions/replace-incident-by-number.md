# TOPdesk: Replace Incident by Number

Replaces an existing incident in TOPdesk by number.

```
PUT https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/replace-incident-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TOPdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/replace-incident-by-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tOPdesk/latest/actions/replace-incident-by-number', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `briefDescription` | string | no | Updated short incident summary. |
| `number` | string | yes | Incident number. |

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

Through the native TOPdesk API, this operation is `PUT /incidents/number/:number` (base URL `https://usatopdesktrial2.topdesk.net/tas/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-incident-by-number.md) for the provider-specific parameters and requirements.

