# Kanban Zone: Get Board

Retrieves a board from Kanban Zone.

```
GET https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-board?connectionId=$CONNECTION_ID&board=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "board": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/get-board?${params}`, {
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
| `board` | string | yes | The board public ID. |
| `includeColumns` | boolean | no | Include columns for the board in the response. |
| `includeCustomFields` | boolean | no | Include custom fields for the board in the response. |

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

Through the native Kanban Zone API, this operation is `GET /board/:board` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-board.md) for the provider-specific parameters and requirements.

