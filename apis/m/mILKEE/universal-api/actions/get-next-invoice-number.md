# MILKEE: Get Next Invoice Number

Retrieves the next invoice number from MILKEE.

```
GET https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/get-next-invoice-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MILKEE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/get-next-invoice-number?connectionId=$CONNECTION_ID&companyId=4640" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "4640"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/get-next-invoice-number?${params}`, {
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
| `companyId` | string | yes | The numeric MILKEE company ID used in the request path. Default: `4640`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string |  |

## Native endpoint

Through the native MILKEE API, this operation is `GET /companies/:companyId/invoices/number` (base URL `https://app.milkee.ch/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-next-invoice-number.md) for the provider-specific parameters and requirements.

