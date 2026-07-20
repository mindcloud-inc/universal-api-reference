# Twilio: List Available Phone Number Countries

Retrieves available phone number countries from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-number-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-number-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-available-phone-number-countries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "countries": [
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
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries[].beta` | boolean |  |
| `countries[].country` | string |  |
| `countries[].countryCode` | string |  |
| `countries[].subresourceUris.local` | string |  |
| `countries[].subresourceUris.mobile` | string |  |
| `countries[].subresourceUris.tollFree` | string |  |
| `countries[].uri` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET /Accounts/:AccountSid/AvailablePhoneNumbers.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-available-phone-number-countries.md) for the provider-specific parameters and requirements.

