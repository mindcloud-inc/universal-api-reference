# Splitwise: Delete Comment

Deletes an expense comment from Splitwise.

```
DELETE https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/delete-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Splitwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/delete-comment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/splitwise/latest/actions/delete-comment?${params}`, {
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
| `id` | number | yes | Splitwise comment ID to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | object | The deleted Splitwise comment. |

## Native endpoint

Through the native Splitwise API, this operation is `POST /delete_comment/[:id]` (base URL `https://secure.splitwise.com/api/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-comment.md) for the provider-specific parameters and requirements.

