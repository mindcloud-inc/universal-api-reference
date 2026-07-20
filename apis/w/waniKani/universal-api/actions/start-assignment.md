# WaniKani: Start Assignment

Starts an assignment in WaniKani.

```
PUT https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/start-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaniKani `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/start-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/waniKani/latest/actions/start-assignment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Unique identifier of the assignment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availableAt": "2026-05-07T12:00:00.000Z",
      "burnedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "hidden": true,
      "passedAt": "2026-05-07T12:00:00.000Z",
      "resurrectedAt": "2026-05-07T12:00:00.000Z",
      "srsStage": 1,
      "startedAt": "2026-05-07T12:00:00.000Z",
      "subjectId": 1,
      "subjectType": "string",
      "unlockedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableAt` | date |  |
| `burnedAt` | date |  |
| `createdAt` | date |  |
| `hidden` | boolean |  |
| `passedAt` | date |  |
| `resurrectedAt` | date |  |
| `srsStage` | number |  |
| `startedAt` | date |  |
| `subjectId` | number |  |
| `subjectType` | string |  |
| `unlockedAt` | date |  |

## Native endpoint

Through the native WaniKani API, this operation is `PUT /assignments/[:id]/start` (base URL `https://api.wanikani.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-assignment.md) for the provider-specific parameters and requirements.

