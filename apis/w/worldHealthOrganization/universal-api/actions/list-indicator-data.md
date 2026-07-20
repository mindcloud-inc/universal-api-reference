# World Health Organization: List Indicator Data

Retrieves data for an indicator from the World Health Organization.

```
GET https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-indicator-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World Health Organization `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-indicator-data?connectionId=$CONNECTION_ID&limit=25&offset=0&indicatorCode=WHOSIS_000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "indicatorCode": "WHOSIS_000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldHealthOrganization/latest/actions/list-indicator-data?${params}`, {
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
| `indicatorCode` | string | yes | WHO indicator code to read observations for, such as WHOSIS_000001. Example: `WHOSIS_000001`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `odataFilter` | string | no | Optional OData $filter expression, for example SpatialDim eq 'BRA' or TimeDim eq 2020. Example: `SpatialDim eq 'BRA'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Date": "2026-05-07T12:00:00.000Z",
      "Dim1": "string",
      "Dim1Type": "string",
      "High": 1,
      "Id": 1,
      "IndicatorCode": "string",
      "Low": 1,
      "NumericValue": 1,
      "ParentLocation": "string",
      "ParentLocationCode": "string",
      "SpatialDim": "string",
      "SpatialDimType": "string",
      "TimeDim": 1,
      "TimeDimensionValue": "string",
      "TimeDimType": "string",
      "Value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Date` | date |  |
| `Dim1` | string |  |
| `Dim1Type` | string |  |
| `High` | number |  |
| `Id` | number |  |
| `IndicatorCode` | string |  |
| `Low` | number |  |
| `NumericValue` | number |  |
| `ParentLocation` | string |  |
| `ParentLocationCode` | string |  |
| `SpatialDim` | string |  |
| `SpatialDimType` | string |  |
| `TimeDim` | number |  |
| `TimeDimensionValue` | string |  |
| `TimeDimType` | string |  |
| `Value` | string |  |

## Native endpoint

Through the native World Health Organization API, this operation is `GET /:indicatorCode` (base URL `https://ghoapi.azureedge.net/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-indicator-data.md) for the provider-specific parameters and requirements.

