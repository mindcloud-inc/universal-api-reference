# Returnless: Detach Return Order Tags

Detaches tags from a return order in Returnless.

```
DELETE https://connect.mindcloud.co/v1/universal/returnless/latest/actions/detach-return-order-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Returnless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/detach-return-order-tags?connectionId=$CONNECTION_ID&returnOrder=string&tags%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "returnOrder": "string",
  "tags[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/returnless/latest/actions/detach-return-order-tags?${params}`, {
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
| `returnOrder` | string | yes | The unique identifier of the return order. |
| `tags[]` | array<string> | yes | The array of tag IDs to detach from the return order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Return order object produced by this mutation. |
| `meta` | object | Execution metadata. |

## Native endpoint

Through the native Returnless API, this operation is `DELETE /2025-01/return-orders/{returnOrder}/tags` (base URL `https://api-v2.returnless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detach-return-order-tags.md) for the provider-specific parameters and requirements.

