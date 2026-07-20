# FEMA: List NFIP Policies

Retrieves NFIP policies from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-policies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-policies?${params}`, {
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
      "countyCode": "string",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "nfipCommunityNumberCurrent": "string",
      "nfipRatedCommunityNumber": "string",
      "occupancyType": 1,
      "policyCost": 1,
      "policyCount": 1,
      "policyEffectiveDate": "2026-05-07T12:00:00.000Z",
      "policyTerminationDate": "2026-05-07T12:00:00.000Z",
      "propertyState": "string",
      "ratedFloodZone": "string",
      "reportedCity": "string",
      "reportedZipCode": "string",
      "totalBuildingInsuranceCoverage": 1,
      "totalContentsInsuranceCoverage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countyCode` | string |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `nfipCommunityNumberCurrent` | string |  |
| `nfipRatedCommunityNumber` | string |  |
| `occupancyType` | number |  |
| `policyCost` | number |  |
| `policyCount` | number |  |
| `policyEffectiveDate` | date |  |
| `policyTerminationDate` | date |  |
| `propertyState` | string |  |
| `ratedFloodZone` | string |  |
| `reportedCity` | string |  |
| `reportedZipCode` | string |  |
| `totalBuildingInsuranceCoverage` | number |  |
| `totalContentsInsuranceCoverage` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/FimaNfipPolicies` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfip-policies.md) for the provider-specific parameters and requirements.

