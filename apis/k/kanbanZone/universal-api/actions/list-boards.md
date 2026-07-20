# Kanban Zone: List Boards

Retrieves boards from Kanban Zone.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-boards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-boards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/list-boards?${params}`, {
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
| `includeArchived` | boolean | no | Include archived boards in the response. |
| `includeColumns` | boolean | no | Include columns for boards in the response. |
| `includeCustomFields` | boolean | no | Include custom fields for boards in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "boards": [
        {}
      ],
      "count": 1,
      "errors": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `boards` | array<object> |  |
| `count` | number |  |
| `errors` | object |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `GET /boards` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-boards.md) for the provider-specific parameters and requirements.

