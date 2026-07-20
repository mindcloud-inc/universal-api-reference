# Cloudmersive Data Validation: Validate Country

Validates country information with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-country?connectionId=$CONNECTION_ID&input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/validate-country?${params}`, {
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
| `input` | object | yes | Country validation request object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CountryFullName": "Ava Chen",
      "CurrencyEnglishName": "Ava Chen",
      "CurrencySymbol": "string",
      "FIPSTwoLetterCode": "string",
      "IsEuropeanUnionMember": true,
      "ISOCurrencyCode": "string",
      "ISOTwoLetterCode": "string",
      "Region": "string",
      "Subregion": "string",
      "Successful": true,
      "ThreeLetterCode": "string",
      "Timezones": [
        {
          "BaseUTCOffset": "string",
          "Name": "Ava Chen",
          "Now": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CountryFullName` | string |  |
| `CurrencyEnglishName` | string |  |
| `CurrencySymbol` | string |  |
| `FIPSTwoLetterCode` | string |  |
| `IsEuropeanUnionMember` | boolean |  |
| `ISOCurrencyCode` | string |  |
| `ISOTwoLetterCode` | string |  |
| `Region` | string |  |
| `Subregion` | string |  |
| `Successful` | boolean |  |
| `ThreeLetterCode` | string |  |
| `Timezones` | array<object> |  |
| `Timezones[].BaseUTCOffset` | string |  |
| `Timezones[].Name` | string |  |
| `Timezones[].Now` | date |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/address/country` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-country.md) for the provider-specific parameters and requirements.

