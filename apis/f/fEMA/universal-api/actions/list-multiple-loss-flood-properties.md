# FEMA: List Multiple Loss Flood Properties

Retrieves multiple loss flood properties from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-multiple-loss-flood-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-multiple-loss-flood-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-multiple-loss-flood-properties?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "county": "string",
      "damagedZipCode": "string",
      "declarationDate": "2026-05-07T12:00:00.000Z",
      "destroyed": true,
      "disasterNumber": 1,
      "fipsCountyCode": "string",
      "fipsStateCode": "string",
      "floodDamage": true,
      "floodInsurance": true,
      "foundationType": "string",
      "highRiskPropertyType": "string",
      "highWaterLocation": "string",
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "numberOfLosses": 1,
      "placeCode": "string",
      "region": 1,
      "residenceType": "string",
      "stateAbbreviation": "string",
      "waterLevel": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `county` | string |  |
| `damagedZipCode` | string |  |
| `declarationDate` | date |  |
| `destroyed` | boolean |  |
| `disasterNumber` | number |  |
| `fipsCountyCode` | string |  |
| `fipsStateCode` | string |  |
| `floodDamage` | boolean |  |
| `floodInsurance` | boolean |  |
| `foundationType` | string |  |
| `highRiskPropertyType` | string |  |
| `highWaterLocation` | string |  |
| `id` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `numberOfLosses` | number |  |
| `placeCode` | string |  |
| `region` | number |  |
| `residenceType` | string |  |
| `stateAbbreviation` | string |  |
| `waterLevel` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/IndividualAssistanceMultipleLossFloodProperties` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-multiple-loss-flood-properties.md) for the provider-specific parameters and requirements.

