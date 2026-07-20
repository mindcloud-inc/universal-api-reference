# Loqate: Validate Phone

Validates a phone number with Loqate.

```
GET https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loqate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-phone?connectionId=$CONNECTION_ID&phone=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phone": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loqate/latest/actions/validate-phone?${params}`, {
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
| `phone` | string | yes | The phone number to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryPrefix": 1,
      "isValid": "string",
      "nationalFormat": "string",
      "networkCode": "string",
      "networkCountry": "string",
      "networkName": "Ava Chen",
      "numberType": "string",
      "phoneNumber": "string",
      "requestProcessed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryPrefix` | number |  |
| `isValid` | string |  |
| `nationalFormat` | string |  |
| `networkCode` | string |  |
| `networkCountry` | string |  |
| `networkName` | string |  |
| `numberType` | string |  |
| `phoneNumber` | string |  |
| `requestProcessed` | boolean |  |

## Native endpoint

Through the native Loqate API, this operation is `GET /PhoneNumberValidation/Interactive/Validate/v2.20/json6.ws` (base URL `https://api.addressy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone.md) for the provider-specific parameters and requirements.

