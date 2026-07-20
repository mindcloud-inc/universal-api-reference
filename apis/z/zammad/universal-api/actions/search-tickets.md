# Zammad: Search Tickets

Finds tickets in Zammad by search query.

```
GET https://connect.mindcloud.co/v1/universal/zammad/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/search-tickets?connectionId=$CONNECTION_ID&query=Help" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Help"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/search-tickets?${params}`, {
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
| `query` | string | yes | Search query. Example: `Help`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articleCount": 1,
      "articleIds": [
        1
      ],
      "checklistId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "groupId": 1,
      "id": 1,
      "number": "string",
      "ownerId": 1,
      "priorityId": 1,
      "stateId": 1,
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
| `articleCount` | number |  |
| `articleIds` | array<number> |  |
| `checklistId` | number |  |
| `createdAt` | date |  |
| `customerId` | number |  |
| `groupId` | number |  |
| `id` | number |  |
| `number` | string |  |
| `ownerId` | number |  |
| `priorityId` | number |  |
| `stateId` | number |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Zammad API, this operation is `GET /tickets/search` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

