# Amazing Marvin: List Today Items

Retrieves today's scheduled items from Amazing Marvin.

```
GET https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/list-today-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/list-today-items?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/list-today-items?${params}`, {
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
| `date` | string | no | Date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "day": "2026-05-07T12:00:00.000Z",
      "db": "string",
      "done": true,
      "dueDate": "2026-05-07T12:00:00.000Z",
      "fieldUpdates": {
        "dueDate": "2026-05-07T12:00:00.000Z"
      },
      "firstScheduled": "2026-05-07T12:00:00.000Z",
      "note": "string",
      "onboard": true,
      "parentId": "string",
      "rank": 1,
      "timeEstimate": 1,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `day` | date |  |
| `db` | string |  |
| `done` | boolean |  |
| `dueDate` | date |  |
| `fieldUpdates.dueDate` | date |  |
| `firstScheduled` | date |  |
| `note` | string |  |
| `onboard` | boolean |  |
| `parentId` | string |  |
| `rank` | number |  |
| `timeEstimate` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `GET /todayItems` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-today-items.md) for the provider-specific parameters and requirements.

