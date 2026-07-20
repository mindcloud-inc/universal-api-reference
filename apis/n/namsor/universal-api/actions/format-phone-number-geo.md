# Namsor: Format Phone Number Geo

Retrieves verified phone number details in Namsor by country.

```
GET https://connect.mindcloud.co/v1/universal/namsor/latest/actions/format-phone-number-geo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Namsor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/namsor/latest/actions/format-phone-number-geo?connectionId=$CONNECTION_ID&countryIso2=string&firstName=Ava&lastName=Chen&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryIso2": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/namsor/latest/actions/format-phone-number-geo?${params}`, {
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
| `countryIso2` | string | yes | Two-letter ISO country code. |
| `firstName` | string | yes | First name. |
| `lastName` | string | yes | Last name. |
| `phoneNumber` | string | yes | Phone number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstName": "Ava",
      "id": "string",
      "internationalPhoneNumberVerified": "string",
      "lastName": "Chen",
      "originCountryIso2": "string",
      "originCountryIso2Alt": "string",
      "phoneCountryCode": 1,
      "phoneCountryCodeAlt": 1,
      "phoneCountryIso2": "string",
      "phoneCountryIso2Alt": "string",
      "phoneCountryIso2Verified": "string",
      "phoneNumber": "string",
      "score": 1,
      "script": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firstName` | string |  |
| `id` | string |  |
| `internationalPhoneNumberVerified` | string |  |
| `lastName` | string |  |
| `originCountryIso2` | string |  |
| `originCountryIso2Alt` | string |  |
| `phoneCountryCode` | number |  |
| `phoneCountryCodeAlt` | number |  |
| `phoneCountryIso2` | string |  |
| `phoneCountryIso2Alt` | string |  |
| `phoneCountryIso2Verified` | string |  |
| `phoneNumber` | string |  |
| `score` | number |  |
| `script` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Namsor API, this operation is `GET /api2/json/phoneCodeGeo/:firstName/:lastName/:phoneNumber/:countryIso2` (base URL `https://v2.namsor.com/NamSorAPIv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/format-phone-number-geo.md) for the provider-specific parameters and requirements.

