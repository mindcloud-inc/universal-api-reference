# Bedrijfsdata.nl: Geocode Address



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/geocode-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/geocode-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/geocode-address?${params}`, {
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
| `countryCode` | string | no | ISO2 country code. |
| `q` | string | no | Address or place query to geocode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "creditsUsedMonth": 1,
      "found": 1,
      "geocoding": [
        {
          "addition": "string",
          "city": "string",
          "countryCode": "string",
          "freeformaddress": "string",
          "lat": 1,
          "letter": "string",
          "lon": 1,
          "municipality": "string",
          "number": 1,
          "postcode": "string",
          "province": "string",
          "provinceCode": "string",
          "street": "string",
          "type": "string"
        }
      ],
      "monthlyCredits": 1,
      "product": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `creditsUsedMonth` | number |  |
| `found` | number |  |
| `geocoding[].addition` | string |  |
| `geocoding[].city` | string |  |
| `geocoding[].countryCode` | string |  |
| `geocoding[].freeformaddress` | string |  |
| `geocoding[].lat` | number |  |
| `geocoding[].letter` | string |  |
| `geocoding[].lon` | number |  |
| `geocoding[].municipality` | string |  |
| `geocoding[].number` | number |  |
| `geocoding[].postcode` | string |  |
| `geocoding[].province` | string |  |
| `geocoding[].provinceCode` | string |  |
| `geocoding[].street` | string |  |
| `geocoding[].type` | string |  |
| `monthlyCredits` | number |  |
| `product` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /geocoding` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/geocode-address.md) for the provider-specific parameters and requirements.

