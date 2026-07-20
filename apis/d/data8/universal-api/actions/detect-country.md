# Data8: Detect Country

Detects a country from contact data in Data8.

```
GET https://connect.mindcloud.co/v1/universal/data8/latest/actions/detect-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Data8 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/data8/latest/actions/detect-country?connectionId=$CONNECTION_ID&request=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/data8/latest/actions/detect-country?${params}`, {
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
| `request` | object | yes | Structured address and contact data used to detect the country. |
| `options` | object | no | Optional settings that control country detection behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CCTLD": "string",
      "CountryISO": "string",
      "CountryName": "Ava Chen",
      "IDC": "string",
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
| `CCTLD` | string |  |
| `CountryISO` | string |  |
| `CountryName` | string |  |
| `IDC` | string |  |
| `Status.CreditsRemaining` | number |  |
| `Status.ErrorMessage` | string |  |
| `Status.Success` | boolean |  |

## Native endpoint

Through the native Data8 API, this operation is `POST /CountryDetection/DetectCountry.json` (base URL `https://webservices.data-8.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-country.md) for the provider-specific parameters and requirements.

