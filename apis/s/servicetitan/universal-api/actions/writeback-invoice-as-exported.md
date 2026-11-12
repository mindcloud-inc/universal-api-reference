# ServiceTitan: Writeback Invoice as Exported



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/writeback-invoice-as-exported
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/writeback-invoice-as-exported" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ],
  "data[].invoiceId": 1,
  "data[].externalId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/writeback-invoice-as-exported', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}],
    "data[].invoiceId": 1,
    "data[].externalId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Root request array. Add one object per invoice to mark as exported. Accepts multiple values as an array. |
| `data[].invoiceId` | number | yes | ServiceTitan invoice ID. Required for every array item. |
| `data[].externalId` | string | yes | External ERP reference, for example Mth=2026-11-01 00:00:00\|ARTrans=534. |
| `data[].externalMessage` | string | no | Optional export result message stored with the ServiceTitan invoice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": "string",
      "invoiceId": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | string | Per-invoice error returned by ServiceTitan when success is false. |
| `invoiceId` | number | ServiceTitan invoice ID processed by the export operation. |
| `success` | boolean | Whether ServiceTitan marked this invoice as exported. |

## Native endpoint

Through the native ServiceTitan API, this operation is `POST accounting/v2/tenant/{{credentials.tenant}}/invoices/markasexported` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/writeback-invoice-as-exported.md) for the provider-specific parameters and requirements.

