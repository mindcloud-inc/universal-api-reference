# Payrexx: Delete Gateway

Deletes a gateway from Payrexx.

```
DELETE https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/delete-gateway
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/delete-gateway?connectionId=$CONNECTION_ID&id=32603338" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "32603338"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/delete-gateway?${params}`, {
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
| `id` | number | yes | ID of gateway payment to delete. Example: `32603338`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `DELETE Gateway/:id/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-gateway.md) for the provider-specific parameters and requirements.

