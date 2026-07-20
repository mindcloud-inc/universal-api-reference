# Conveyor: List Interactions

Retrieves interactions for a program from Conveyor.

```
GET https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-interactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-interactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/list-interactions?${params}`, {
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
| `type` | string | no | Interaction type filter. |
| `createdAtStart` | date | no | Start of created-at date range. |
| `createdAtEnd` | date | no | End of created-at date range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interactions": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "type": "string"
        }
      ],
      "page": 1,
      "per_page": 1,
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interactions` | array<object> |  |
| `interactions[].created_at` | date |  |
| `interactions[].id` | string |  |
| `interactions[].type` | string |  |
| `page` | number |  |
| `per_page` | number |  |
| `total_pages` | number |  |

## Native endpoint

Through the native Conveyor API, this operation is `GET /v2/interactions` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-interactions.md) for the provider-specific parameters and requirements.

