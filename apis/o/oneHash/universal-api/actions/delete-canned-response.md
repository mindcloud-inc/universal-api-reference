# OneHash: Delete Canned Response

Deletes an existing canned response from OneHash.

```
DELETE https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/delete-canned-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneHash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/delete-canned-response?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneHash/latest/actions/delete-canned-response?${params}`, {
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
| `accountId` | string | no | OneHash Chat account id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OneHash API returns.

## Native endpoint

Through the native OneHash API, this operation is `DELETE /api/v1/accounts/:accountId/canned_responses/:id` (base URL `https://chat.onehash.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-canned-response.md) for the provider-specific parameters and requirements.

