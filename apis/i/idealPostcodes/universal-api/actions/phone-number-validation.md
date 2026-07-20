# Ideal Postcodes: Phone Number Validation

Validates a phone number in Ideal Postcodes.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/phone-number-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/phone-number-validation?connectionId=$CONNECTION_ID&query=02071128019" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "02071128019"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/phone-number-validation?${params}`, {
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
| `query` | string | yes | Phone number to validate, including a country code when possible. Default: `02071128019`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currentCarrier` | boolean | no | Set to true to request the current network carrier. |
| `tags` | string | no | Comma-separated tags to associate with the validation request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "currentCarrier": {
        "country": "string",
        "name": "Ava Chen",
        "networkCode": "string",
        "networkType": "string"
      },
      "internationalFormat": "string",
      "isoCountry": "string",
      "isoCountry2": "string",
      "nationalFormat": "string",
      "originalCarrier": {
        "country": "string",
        "name": "Ava Chen",
        "networkCode": "string",
        "networkType": "string"
      },
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `currentCarrier.country` | string |  |
| `currentCarrier.name` | string |  |
| `currentCarrier.networkCode` | string |  |
| `currentCarrier.networkType` | string |  |
| `internationalFormat` | string |  |
| `isoCountry` | string |  |
| `isoCountry2` | string |  |
| `nationalFormat` | string |  |
| `originalCarrier.country` | string |  |
| `originalCarrier.name` | string |  |
| `originalCarrier.networkCode` | string |  |
| `originalCarrier.networkType` | string |  |
| `valid` | boolean |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /phone_numbers` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/phone-number-validation.md) for the provider-specific parameters and requirements.

