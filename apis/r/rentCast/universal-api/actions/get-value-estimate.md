# RentCast: Get Value Estimate

Retrieves a property value estimate from RentCast.

```
GET https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-value-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RentCast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-value-estimate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentCast/latest/actions/get-value-estimate?${params}`, {
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
| `address` | string | no | The full property address in the format Street, City, State, Zip. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `latitude` | number | no | Latitude of the subject property when using coordinates instead of a full address. |
| `longitude` | number | no | Longitude of the subject property when using coordinates instead of a full address. |
| `propertyType` | list<string> | no | The subject property type. One of: `Apartment`, `Condo`, `Land`, `Manufactured`, `Multi-Family`, `Single Family`, `Townhouse`. |
| `bedrooms` | number | no | The number of bedrooms in the subject property. |
| `bathrooms` | number | no | The number of bathrooms in the subject property. |
| `squareFootage` | number | no | The total living area size of the subject property in square feet. |
| `maxRadius` | number | no | The maximum distance in miles between comparable listings and the subject property. |
| `daysOld` | number | no | The maximum number of days since comparable listings were last seen on the market. |
| `compCount` | number | no | The number of comparable listings to use when calculating the estimate. |
| `lookupSubjectAttributes` | boolean | no | When enabled, RentCast attempts to look up subject property attributes to find more relevant comps. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comparables": [
        {}
      ],
      "latitude": 1,
      "longitude": 1,
      "price": 1,
      "priceRangeHigh": 1,
      "priceRangeLow": 1,
      "subjectProperty": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comparables` | array<object> |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `price` | number |  |
| `priceRangeHigh` | number |  |
| `priceRangeLow` | number |  |
| `subjectProperty` | object |  |

## Native endpoint

Through the native RentCast API, this operation is `GET /avm/value` (base URL `https://api.rentcast.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-value-estimate.md) for the provider-specific parameters and requirements.

