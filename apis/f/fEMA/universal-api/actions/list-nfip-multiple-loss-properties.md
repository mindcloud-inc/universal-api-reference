# FEMA: List NFIP Multiple Loss Properties

Retrieves NFIP multiple loss properties from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-multiple-loss-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-multiple-loss-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-multiple-loss-properties?${params}`, {
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
      "asOfDate": "2026-05-07T12:00:00.000Z",
      "censusBlockGroup": "string",
      "communityIdNumber": "string",
      "communityName": "Ava Chen",
      "county": "string",
      "fipsCountyCode": "string",
      "floodZone": "string",
      "fmaRl": true,
      "fmaSrl": true,
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "mostRecentDateofLoss": "2026-05-07T12:00:00.000Z",
      "nfipRl": true,
      "nfipSrl": true,
      "reportedCity": "string",
      "state": "string",
      "stateAbbreviation": "string",
      "totalLosses": 1,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asOfDate` | date |  |
| `censusBlockGroup` | string |  |
| `communityIdNumber` | string |  |
| `communityName` | string |  |
| `county` | string |  |
| `fipsCountyCode` | string |  |
| `floodZone` | string |  |
| `fmaRl` | boolean |  |
| `fmaSrl` | boolean |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `mostRecentDateofLoss` | date |  |
| `nfipRl` | boolean |  |
| `nfipSrl` | boolean |  |
| `reportedCity` | string |  |
| `state` | string |  |
| `stateAbbreviation` | string |  |
| `totalLosses` | number |  |
| `zipCode` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/NfipMultipleLossProperties` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfip-multiple-loss-properties.md) for the provider-specific parameters and requirements.

