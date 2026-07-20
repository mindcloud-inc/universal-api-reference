# Twilio: List Available Phone Numbers Local

Finds available local phone numbers in Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-numbers-local
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-numbers-local?connectionId=$CONNECTION_ID&limit=25&offset=0&countryCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "countryCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-numbers-local?${params}`, {
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
| `areaCode` | string | no |  |
| `contains` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availablePhoneNumbers": [
        {
          "addressRequirements": "string",
          "beta": true,
          "capabilities": {
            "mms": true,
            "sms": true,
            "voice": true
          },
          "friendlyName": "Ava Chen",
          "isoCountry": "string",
          "lata": "string",
          "latitude": "string",
          "locality": "string",
          "longitude": "string",
          "phoneNumber": "string",
          "postalCode": "string",
          "rateCenter": "string",
          "region": "string"
        }
      ],
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availablePhoneNumbers[].addressRequirements` | string |  |
| `availablePhoneNumbers[].beta` | boolean |  |
| `availablePhoneNumbers[].capabilities.mms` | boolean |  |
| `availablePhoneNumbers[].capabilities.sms` | boolean |  |
| `availablePhoneNumbers[].capabilities.voice` | boolean |  |
| `availablePhoneNumbers[].friendlyName` | string |  |
| `availablePhoneNumbers[].isoCountry` | string |  |
| `availablePhoneNumbers[].lata` | string |  |
| `availablePhoneNumbers[].latitude` | string |  |
| `availablePhoneNumbers[].locality` | string |  |
| `availablePhoneNumbers[].longitude` | string |  |
| `availablePhoneNumbers[].phoneNumber` | string |  |
| `availablePhoneNumbers[].postalCode` | string |  |
| `availablePhoneNumbers[].rateCenter` | string |  |
| `availablePhoneNumbers[].region` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET /Accounts/:AccountSid/AvailablePhoneNumbers/:CountryCode/Local.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-available-phone-numbers-local.md) for the provider-specific parameters and requirements.

