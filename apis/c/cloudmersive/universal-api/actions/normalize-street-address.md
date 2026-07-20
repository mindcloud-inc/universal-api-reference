# Cloudmersive: Normalize Street Address

Normalizes a street address in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/normalize-street-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/normalize-street-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/normalize-street-address?${params}`, {
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
| `City` | string | no | City for the address. |
| `CountryCode` | string | no | Optional two-letter country code. |
| `CountryFullName` | string | no | Optional country name. |
| `PostalCode` | string | no | Optional postal or ZIP code. |
| `StateOrProvince` | string | no | State or province for the address. |
| `StreetAddress` | string | no | Street address to normalize. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "building": "string",
      "city": "string",
      "countryFullName": "Ava Chen",
      "isoTwoLetterCode": "string",
      "latitude": 1,
      "longitude": 1,
      "postalCode": "string",
      "stateOrProvince": "string",
      "street": "string",
      "streetNumber": "string",
      "validAddress": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `building` | string |  |
| `city` | string |  |
| `countryFullName` | string |  |
| `isoTwoLetterCode` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `postalCode` | string |  |
| `stateOrProvince` | string |  |
| `street` | string |  |
| `streetNumber` | string |  |
| `validAddress` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/street-address/normalize` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/normalize-street-address.md) for the provider-specific parameters and requirements.

