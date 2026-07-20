# Billage: Get Invoice by Reference

Retrieves an invoice from Billage by reference code.

```
GET https://connect.mindcloud.co/v1/universal/billage/latest/actions/get-invoice-by-reference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billage/latest/actions/get-invoice-by-reference?connectionId=$CONNECTION_ID&serie=string&ref=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serie": "string",
  "ref": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billage/latest/actions/get-invoice-by-reference?${params}`, {
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
| `year` | number | no | Invoice year |
| `serie` | string | yes | Invoice serie |
| `ref` | string | yes | Invoice reference |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billage API returns.

## Native endpoint

Through the native Billage API, this operation is `GET /v2/invoices/by-ref` (base URL `https://app.getbillage.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-by-reference.md) for the provider-specific parameters and requirements.

