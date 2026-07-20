# Cloudmersive Data Validation: Validate Phone Number

Validates a phone number with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-phone-number?connectionId=$CONNECTION_ID&value=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "value": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-phone-number?${params}`, {
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
| `value` | object | yes | Phone number validation request object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CountryCode": "string",
      "CountryName": "Ava Chen",
      "E164Format": "string",
      "InternationalFormat": "string",
      "IsValid": true,
      "NationalFormat": "string",
      "PhoneNumberType": "string",
      "Successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CountryCode` | string |  |
| `CountryName` | string |  |
| `E164Format` | string |  |
| `InternationalFormat` | string |  |
| `IsValid` | boolean |  |
| `NationalFormat` | string |  |
| `PhoneNumberType` | string |  |
| `Successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/phonenumber/basic` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number.md) for the provider-specific parameters and requirements.

