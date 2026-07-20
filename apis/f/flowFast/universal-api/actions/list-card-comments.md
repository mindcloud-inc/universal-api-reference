# FlowFast: List Card Comments

Retrieves comments from a card in FlowFast.

```
GET https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/list-card-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowFast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/list-card-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/list-card-comments?${params}`, {
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
| `cardId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardId": 1,
      "id": 1,
      "text": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardId` | number |  |
| `id` | number |  |
| `text` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native FlowFast API, this operation is `GET /cards/:cardId/comments` (base URL `https://apps.flowfast.io/api/latest/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-card-comments.md) for the provider-specific parameters and requirements.

