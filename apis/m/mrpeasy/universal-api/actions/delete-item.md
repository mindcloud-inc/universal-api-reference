# MRPeasy: Delete Item

Deletes an existing stock item from MRPeasy.

```
DELETE https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/delete-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/delete-item?connectionId=$CONNECTION_ID&articleId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "articleId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/delete-item?${params}`, {
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
| `articleId` | number | yes | MRPeasy article ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `DELETE /items/{{articleId}}` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-item.md) for the provider-specific parameters and requirements.

