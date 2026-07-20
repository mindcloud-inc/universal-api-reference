# FEMA: List NFIP Claims

Retrieves NFIP claims from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-claims
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-claims?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-claims?${params}`, {
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
      "amountPaidOnBuildingClaim": 1,
      "amountPaidOnContentsClaim": 1,
      "asOfDate": "2026-05-07T12:00:00.000Z",
      "countyCode": "string",
      "dateOfLoss": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "nfipRatedCommunityNumber": "string",
      "occupancyType": 1,
      "policyCount": 1,
      "ratedFloodZone": "string",
      "reportedCity": "string",
      "reportedZipCode": "string",
      "state": "string",
      "yearOfLoss": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountPaidOnBuildingClaim` | number |  |
| `amountPaidOnContentsClaim` | number |  |
| `asOfDate` | date |  |
| `countyCode` | string |  |
| `dateOfLoss` | date |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `nfipRatedCommunityNumber` | string |  |
| `occupancyType` | number |  |
| `policyCount` | number |  |
| `ratedFloodZone` | string |  |
| `reportedCity` | string |  |
| `reportedZipCode` | string |  |
| `state` | string |  |
| `yearOfLoss` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/FimaNfipClaims` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfip-claims.md) for the provider-specific parameters and requirements.

