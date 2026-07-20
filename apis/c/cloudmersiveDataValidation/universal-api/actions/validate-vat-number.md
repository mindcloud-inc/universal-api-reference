# Cloudmersive Data Validation: Validate VAT Number

Validates a VAT number with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-vat-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-vat-number?${params}`, {
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
| `input` | object | yes | VAT lookup request object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "BusinessAddress": "string",
      "BusinessBuilding": "string",
      "BusinessCity": "string",
      "BusinessCountry": "string",
      "BusinessName": "Ava Chen",
      "BusinessPostalCode": "string",
      "BusinessStateOrProvince": "string",
      "BusinessStreet": "string",
      "BusinessStreetNumber": "string",
      "CountryCode": "string",
      "IsValid": true,
      "VatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `BusinessAddress` | string |  |
| `BusinessBuilding` | string |  |
| `BusinessCity` | string |  |
| `BusinessCountry` | string |  |
| `BusinessName` | string |  |
| `BusinessPostalCode` | string |  |
| `BusinessStateOrProvince` | string |  |
| `BusinessStreet` | string |  |
| `BusinessStreetNumber` | string |  |
| `CountryCode` | string |  |
| `IsValid` | boolean |  |
| `VatNumber` | string |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/vat/lookup` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-vat-number.md) for the provider-specific parameters and requirements.

