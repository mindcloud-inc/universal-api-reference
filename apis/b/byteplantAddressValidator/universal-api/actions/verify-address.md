# Byteplant Address Validator: Verify Address

Retrieves address validation results from Byteplant Address Validator.

```
GET https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/verify-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Byteplant Address Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/verify-address?connectionId=$CONNECTION_ID&streetAddress=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "streetAddress": "string",
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteplantAddressValidator/latest/actions/verify-address?${params}`, {
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
| `streetAddress` | string | yes | Street, house number, or complete address. |
| `countryCode` | string | yes | Two-letter ISO 3166-1 country code. Use XX for international. |
| `city` | string | no | City or locality. |
| `state` | string | no | State or province. |
| `postalCode` | string | no | ZIP or postal code. |
| `streetNumber` | string | no | House number or building number, when separate from the street address. |
| `additionalAddressInfo` | string | no | Building, unit, apartment, floor, or other extra address details. |
| `geocoding` | boolean | no | Include latitude and longitude in the response. Default: `false`. |
| `locale` | string | no | Output language for countries with multiple postal languages. |
| `outputCharset` | string | no | Output character set. Default: `utf-8`. |
| `timeout` | number | no | Request timeout in seconds. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressline1": "string",
      "addresslinelast": "string",
      "city": "string",
      "corrections": "string",
      "cost": 1,
      "country": "string",
      "county": "string",
      "formattedaddress": "string",
      "latitude": 1,
      "longitude": 1,
      "postalcode": "string",
      "ratelimit_remain": 1,
      "ratelimit_seconds": 1,
      "rdi": "string",
      "state": "string",
      "status": "string",
      "street": "string",
      "streetnumber": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressline1` | string | Normalized first address line. |
| `addresslinelast` | string | Normalized final address line. |
| `city` | string | Normalized city. |
| `corrections` | string | Correction codes returned by Byteplant. |
| `cost` | number | Credits consumed by the request. |
| `country` | string | Normalized ISO country code. |
| `county` | string | County or regional subdivision. |
| `formattedaddress` | string | Normalized full address. |
| `latitude` | number | Latitude when geocoding is enabled. |
| `longitude` | number | Longitude when geocoding is enabled. |
| `postalcode` | string | Normalized postal code. |
| `ratelimit_remain` | number | Remaining requests in the current rate-limit window. |
| `ratelimit_seconds` | number | Seconds remaining in the current rate-limit window. |
| `rdi` | string | Residential delivery indicator. |
| `state` | string | Normalized state or province. |
| `status` | string | Byteplant validation status. |
| `street` | string | Normalized street name. |
| `streetnumber` | string | Normalized street number. |
| `type` | string | Address type code. |

## Native endpoint

Through the native Byteplant Address Validator API, this operation is `GET /api/verify` (base URL `https://api.address-validator.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-address.md) for the provider-specific parameters and requirements.

