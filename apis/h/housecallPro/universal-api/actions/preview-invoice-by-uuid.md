# Housecall Pro: Preview Invoice by UUID



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/preview-invoice-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/preview-invoice-by-uuid?connectionId=$CONNECTION_ID&uuid=invoice_b0068ccfac5e47309ddfe99d5a51f578" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "invoice_b0068ccfac5e47309ddfe99d5a51f578"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/preview-invoice-by-uuid?${params}`, {
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
| `uuid` | string | yes | The UUID of the invoice to preview. Example: `invoice_b0068ccfac5e47309ddfe99d5a51f578`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary HTML preview bytes. |
| `type` | string | Buffer marker for the HTML preview payload. |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /api/invoices/:uuid/preview` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-invoice-by-uuid.md) for the provider-specific parameters and requirements.

