# Byteplant Address Validator: Start Bulk Address Validation

Creates a bulk address validation task in Byteplant Address Validator.

```
POST https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/start-bulk-address-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Byteplant Address Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/start-bulk-address-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressesCsv": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/start-bulk-address-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressesCsv": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addressesCsv` | string | yes | CSV content with address rows for bulk validation. |
| `countryCode` | string | no | Optional two-letter ISO 3166-1 country code. Use XX for international. |
| `geocoding` | boolean | no | Include latitude and longitude in bulk validation results. Default: `false`. |
| `outputCharset` | string | no | Output character set. Default: `utf-8`. |
| `locale` | string | no | Output language for countries with multiple postal languages. |
| `taskName` | string | no | Optional name for the bulk validation task. |
| `notifyEmail` | string | no | Optional email address to receive task completion notifications. |
| `notifyUrl` | string | no | Optional URL to receive task completion notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "info": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `info` | string | Task identifier when accepted, or provider error information when the request is rejected. |
| `status` | string | Bulk task submission status. |

## Native endpoint

Through the native Byteplant Address Validator API, this operation is `POST /api/bulk-verify` (base URL `https://api.address-validator.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-bulk-address-validation.md) for the provider-specific parameters and requirements.

