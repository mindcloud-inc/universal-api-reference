# Precisely: Get PreciselyID By Address

Retrieves a PreciselyID for an address in Precisely.

```
GET https://connect.mindcloud.co/v1/universal/precisely/latest/actions/get-preciselyid-by-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Precisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/precisely/latest/actions/get-preciselyid-by-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/precisely/latest/actions/get-preciselyid-by-address?${params}`, {
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
| `address` | string | yes | Single-line address to resolve to a PreciselyID. |
| `country` | string | no | ISO country code or country name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "key": "string",
      "matchedAddress": {
        "addressLastLine": "string",
        "addressNumber": "string",
        "areaName1": "Ava Chen",
        "areaName2": "Ava Chen",
        "areaName3": "Ava Chen",
        "country": "string",
        "formattedAddress": "string",
        "mainAddressLine": "string",
        "postCode": "string",
        "postCodeExt": "string",
        "streetName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `key` | string | PreciselyID returned for the input address. |
| `matchedAddress.addressLastLine` | string | City, region, and postal line. |
| `matchedAddress.addressNumber` | string | Address number. |
| `matchedAddress.areaName1` | string | Top-level administrative area, typically state or province. |
| `matchedAddress.areaName2` | string | Secondary administrative area, typically county or district. |
| `matchedAddress.areaName3` | string | City or locality name. |
| `matchedAddress.country` | string | Country code or country name. |
| `matchedAddress.formattedAddress` | string | Fully formatted matched address. |
| `matchedAddress.mainAddressLine` | string | Primary street-address line. |
| `matchedAddress.postCode` | string | Postal code. |
| `matchedAddress.postCodeExt` | string | Postal code extension. |
| `matchedAddress.streetName` | string | Street name. |

## Native endpoint

Through the native Precisely API, this operation is `GET /geocode/v1/key/byaddress` (base URL `https://api.precisely.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-preciselyid-by-address.md) for the provider-specific parameters and requirements.

