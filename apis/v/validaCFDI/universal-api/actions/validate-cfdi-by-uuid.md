# ValidaCFDI: Validate CFDI by UUID

Validates a CFDI by UUID in ValidaCFDI.

```
GET https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/validate-cfdi-by-uuid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ValidaCFDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/validate-cfdi-by-uuid?connectionId=$CONNECTION_ID&uuid=string&rfcEmisor=string&rfcReceptor=string&total=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string",
  "rfcEmisor": "string",
  "rfcReceptor": "string",
  "total": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/validaCFDI/latest/actions/validate-cfdi-by-uuid?${params}`, {
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
| `uuid` | string | yes | CFDI UUID to validate. |
| `rfcEmisor` | string | yes | RFC of the CFDI issuer. |
| `rfcReceptor` | string | yes | RFC of the CFDI receiver. |
| `total` | number | yes | Total invoice amount for validation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cfdiData": {
        "codigoEstatus": "string",
        "esCancelable": "string",
        "estadoCancelacion": "string",
        "estadoCfdi": "string",
        "rfcEmisor": "string",
        "rfcReceptor": "string",
        "total": 1,
        "uuid": "string"
      },
      "errors": [
        "string"
      ],
      "status": "string",
      "valid": true,
      "validationTimestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cfdiData` | object | Structured CFDI validation details. |
| `cfdiData.codigoEstatus` | string | Provider status code and message. |
| `cfdiData.esCancelable` | string | Whether the CFDI can be cancelled. |
| `cfdiData.estadoCancelacion` | string | Cancellation status when available. |
| `cfdiData.estadoCfdi` | string | SAT CFDI status. |
| `cfdiData.rfcEmisor` | string | RFC of the invoice issuer from successful validation payloads. |
| `cfdiData.rfcReceptor` | string | RFC of the invoice receiver from successful validation payloads. |
| `cfdiData.total` | number | Invoice total from successful validation payloads. |
| `cfdiData.uuid` | string | CFDI UUID that was validated. |
| `errors` | array<string> | Validation errors when the CFDI could not be confirmed. |
| `status` | string | Validation status returned by the provider. |
| `valid` | boolean | Whether the CFDI validation succeeded. |
| `validationTimestamp` | date | Timestamp of the validation result. |

## Native endpoint

Through the native ValidaCFDI API, this operation is `POST /validate` (base URL `https://api.valida-cfdi.com.mx/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-cfdi-by-uuid.md) for the provider-specific parameters and requirements.

