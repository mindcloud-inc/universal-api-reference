# Trafft: Delete Customer

Deletes an existing customer from Trafft.

```
DELETE https://connect.mindcloud.co/v1/universal/trafft/latest/actions/delete-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trafft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/delete-customer?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trafft/latest/actions/delete-customer?${params}`, {
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
| `id` | number | yes | The Trafft customer ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Trafft API returns.

## Native endpoint

Through the native Trafft API, this operation is `DELETE /customers/:id` (base URL `https://mindcloud.admin.trafft.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-customer.md) for the provider-specific parameters and requirements.

