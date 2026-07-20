# Xata: Retrieve branch logs



```
POST https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-logs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationID": "string",
  "projectID": "string",
  "branchID": "string",
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xata/latest/actions/branch-logs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationID": "string",
    "projectID": "string",
    "branchID": "string",
    "start": "2026-05-07T12:00:00.000Z",
    "end": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationID` | string | yes |  |
| `projectID` | string | yes |  |
| `branchID` | string | yes |  |
| `start` | date | yes | Start time |
| `end` | date | yes | End time |
| `filters[]` | array | no | Filters applied to log entries. Multiple filters are combined with AND. |
| `limit` | number | no |  |
| `cursor` | string | no | Pagination cursor from a previous response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "logs": [
        {}
      ],
      "nextCursor": "string",
      "start": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date |  |
| `logs` | array<object> |  |
| `nextCursor` | string | Pagination cursor for the next page |
| `start` | date |  |

## Native endpoint

Through the native Xata API, this operation is `POST /organizations/:organizationID/projects/:projectID/branches/:branchID/logs` (base URL `https://api.xata.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/branch-logs.md) for the provider-specific parameters and requirements.

