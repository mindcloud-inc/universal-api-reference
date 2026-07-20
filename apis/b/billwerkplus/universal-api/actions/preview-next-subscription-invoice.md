# Billwerkplus: Preview Next Subscription Invoice

Retrieves the next invoice preview for a Billwerkplus subscription.

```
GET https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/preview-next-subscription-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/preview-next-subscription-invoice?connectionId=$CONNECTION_ID&handle=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handle": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/preview-next-subscription-invoice?${params}`, {
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
| `handle` | string | yes | Subscription handle. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billwerkplus API returns.

## Native endpoint

Through the native Billwerkplus API, this operation is `GET /subscription/:handle/next_invoice_preview` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-next-subscription-invoice.md) for the provider-specific parameters and requirements.

