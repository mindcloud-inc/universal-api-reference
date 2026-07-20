# Data8: Validate Phone Number

Validates a phone number with Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-phone-number?connectionId=$CONNECTION_ID&telephoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "telephoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/validate-phone-number?${params}`, {
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
| `telephoneNumber` | string | yes | The telephone number to validate. |
| `defaultCountry` | string | no | Country code to assume when the number has no international dialling code. |
| `options` | object | no | Optional settings that control validation behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": {
        "CountryCode": "string",
        "Provider": "string",
        "TelephoneNumber": "string",
        "ValidationLevel": "string",
        "ValidationResult": "string"
      },
      "Status": {
        "CreditsRemaining": 1,
        "ErrorMessage": "string",
        "Success": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result.CountryCode` | string |  |
| `Result.Provider` | string |  |
| `Result.TelephoneNumber` | string |  |
| `Result.ValidationLevel` | string |  |
| `Result.ValidationResult` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /PhoneValidation/IsValid.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-phone-number.md) for the provider-specific parameters and requirements.

