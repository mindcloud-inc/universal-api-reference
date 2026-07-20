# Chat Aid: Delete Custom Sources by IDs

Deletes custom sources from Chat Aid by IDs or filters.

```
DELETE https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/delete-custom-sources-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chat Aid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/delete-custom-sources-by-ids?connectionId=$CONNECTION_ID&ids%5B%5D=65e1c08202791119fbe1d476" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids[]": "65e1c08202791119fbe1d476"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatAid/latest/actions/delete-custom-sources-by-ids?${params}`, {
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
| `ids[]` | array<string> | yes | Array of custom source IDs to delete. Example: `65e1c08202791119fbe1d476`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedCount": 1,
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedCount` | number |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Chat Aid API, this operation is `DELETE /external/sources/custom` (base URL `https://api.chataid.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-custom-sources-by-ids.md) for the provider-specific parameters and requirements.

