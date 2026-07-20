# Dovetail: Delete Doc

Deletes an existing doc from Dovetail.

```
DELETE https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/delete-doc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dovetail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/delete-doc?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dovetail/latest/actions/delete-doc?${params}`, {
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
| `docId` | string | yes | Doc ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dovetail API returns.

## Native endpoint

Through the native Dovetail API, this operation is `DELETE /v1/docs/:docId` (base URL `https://dovetail.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-doc.md) for the provider-specific parameters and requirements.

