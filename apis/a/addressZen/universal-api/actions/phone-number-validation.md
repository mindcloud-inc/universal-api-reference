# AddressZen: Phone Number Validation

Retrieves phone number validation details from AddressZen.

```
GET https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/phone-number-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddressZen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/phone-number-validation?connectionId=$CONNECTION_ID&query=%2B14155552671" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "+14155552671"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/phone-number-validation?${params}`, {
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
| `query` | string | yes | Phone number to validate Example: `+14155552671`. |

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

Through the native AddressZen API, this operation is `GET /phone_numbers` (base URL `https://api.addresszen.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/phone-number-validation.md) for the provider-specific parameters and requirements.

