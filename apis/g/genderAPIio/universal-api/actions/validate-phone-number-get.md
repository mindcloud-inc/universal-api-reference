# GenderAPI.io: Validate Phone Number (GET)

Retrieves phone validation details from GenderAPI.io.

```
GET https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/validate-phone-number-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GenderAPI.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/validate-phone-number-get?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/genderAPIio/latest/actions/validate-phone-number-get?${params}`, {
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
| `number` | string | yes |  |
| `address` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areaCode": "string",
      "country": "string",
      "countryCode": 1,
      "duration": "string",
      "e164": "string",
      "expires": 1,
      "international": "string",
      "isGeographical": true,
      "isPossible": true,
      "isValid": true,
      "location": "string",
      "national": "string",
      "nationalSignificantNumber": "string",
      "numberType": "string",
      "rawInput": "string",
      "regionCode": "string",
      "remaining_credits": 1,
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areaCode` | string | Detected area code. |
| `country` | string | Full country name. |
| `countryCode` | number | International dialing country code. |
| `duration` | string | Processing time for the request. |
| `e164` | string | Phone number in E.164 format. |
| `expires` | number | Unix timestamp for plan expiration. |
| `international` | string | Formatted international phone number. |
| `isGeographical` | boolean | Whether the number is tied to a geographic area. |
| `isPossible` | boolean | Whether the number could exist structurally. |
| `isValid` | boolean | Whether the number is valid. |
| `location` | string | Detected geographic location. |
| `national` | string | Formatted national phone number. |
| `nationalSignificantNumber` | string | National number without country code. |
| `numberType` | string | The detected phone number type. |
| `rawInput` | string | Original phone number input. |
| `regionCode` | string | ISO 3166-1 alpha-2 region code. |
| `remaining_credits` | number | The number of credits remaining after the request. |
| `status` | boolean | Whether the request was successful. |

## Native endpoint

Through the native GenderAPI.io API, this operation is `GET /api/phone` (base URL `https://api.genderapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number-get.md) for the provider-specific parameters and requirements.

