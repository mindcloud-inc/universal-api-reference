# FlowFast: Delete Card

Deletes an existing card from FlowFast.

```
DELETE https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/delete-card
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FlowFast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/delete-card?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flowFast/latest/actions/delete-card?${params}`, {
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
      "archived": true,
      "boardId": 1,
      "id": 1,
      "title": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `boardId` | number |  |
| `id` | number |  |
| `title` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native FlowFast API, this operation is `DELETE /cards/:cardId` (base URL `https://apps.flowfast.io/api/latest/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-card.md) for the provider-specific parameters and requirements.

