# Twilio: Get Available Phone Number Country

Retrieves available phone number details for a country in Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-available-phone-number-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-available-phone-number-country?connectionId=$CONNECTION_ID&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-available-phone-number-country?${params}`, {
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
| `countryCode` | string | yes | Default: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "beta": true,
      "country": "string",
      "countryCode": "string",
      "subresourceUris": {
        "local": "string",
        "mobile": "string",
        "tollFree": "string"
      },
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beta` | boolean |  |
| `country` | string |  |
| `countryCode` | string |  |
| `subresourceUris.local` | string |  |
| `subresourceUris.mobile` | string |  |
| `subresourceUris.tollFree` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET /Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-available-phone-number-country.md) for the provider-specific parameters and requirements.

