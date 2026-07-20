# Cloudmersive: Validate Country

Validates country information in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-country
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-country?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-country?${params}`, {
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
| `RawCountryInput` | string | no | Country code or country name to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryFullName": "Ava Chen",
      "isEuropeanUnionMember": true,
      "isoCurrencyCode": "string",
      "isoTwoLetterCode": "string",
      "region": "string",
      "subregion": "string",
      "successful": true,
      "threeLetterCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryFullName` | string |  |
| `isEuropeanUnionMember` | boolean |  |
| `isoCurrencyCode` | string |  |
| `isoTwoLetterCode` | string |  |
| `region` | string |  |
| `subregion` | string |  |
| `successful` | boolean |  |
| `threeLetterCode` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/country` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-country.md) for the provider-specific parameters and requirements.

