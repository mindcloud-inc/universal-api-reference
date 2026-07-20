# LoopedIn: List Feedback for Board

Retrieves feedback for a feedback board in LoopedIn.

```
GET https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-feedback-for-board
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LoopedIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-feedback-for-board?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-feedback-for-board?${params}`, {
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
| `id` | string | yes | The LoopedIn feedback board ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "feedback": [
        {}
      ],
      "id": "string",
      "public": true,
      "title": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `feedback` | array<object> |  |
| `id` | string |  |
| `public` | boolean |  |
| `title` | string |  |
| `workspace` | string |  |

## Native endpoint

Through the native LoopedIn API, this operation is `GET /feedback-boards/:id/feedback` (base URL `https://api.loopedin.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feedback-for-board.md) for the provider-specific parameters and requirements.

