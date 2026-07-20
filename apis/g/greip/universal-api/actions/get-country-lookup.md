# Greip - Fraud Prevention: Get Country Lookup

Retrieves country lookup data from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-country-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-country-lookup?connectionId=$CONNECTION_ID&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "countryCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-country-lookup?${params}`, {
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
| `countryCode` | string | yes | The ISO 3166-1 alpha-2 country code to look up. |
| `params` | string | no | Comma-separated modules to include, such as language, flag, currency, or timezone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capital": "string",
      "continentCode": "string",
      "continentGeoNameID": 1,
      "continentName": "Ava Chen",
      "countryCode": "string",
      "countryGeoNameID": 1,
      "countryIsEU": true,
      "countryName": "Ava Chen",
      "countryNeighbours": "string",
      "phoneCode": "string",
      "population": 1,
      "tld": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capital` | string |  |
| `continentCode` | string |  |
| `continentGeoNameID` | number |  |
| `continentName` | string |  |
| `countryCode` | string |  |
| `countryGeoNameID` | number |  |
| `countryIsEU` | boolean |  |
| `countryName` | string |  |
| `countryNeighbours` | string |  |
| `phoneCode` | string |  |
| `population` | number |  |
| `tld` | string |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/country` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-lookup.md) for the provider-specific parameters and requirements.

