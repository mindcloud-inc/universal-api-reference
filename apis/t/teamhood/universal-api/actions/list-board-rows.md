# Teamhood: List Board Rows

Retrieves rows for a Teamhood board.

```
GET https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-board-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teamhood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-board-rows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamhood/latest/actions/list-board-rows?${params}`, {
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
| `boardId` | string | no | The Teamhood board ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rows": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rows` | array<object> | Rows configured on the Teamhood board. |

## Native endpoint

Through the native Teamhood API, this operation is `GET /boards/:boardId/rows` (base URL `https://api-mindcloud1.teamhood.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-board-rows.md) for the provider-specific parameters and requirements.

