# FEMA: List HMA Subapplications by NFIP CRS Communities

Retrieves HMA subapplications for NFIP CRS communities.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplications-by-nfip-crs-communities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplications-by-nfip-crs-communities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplications-by-nfip-crs-communities?${params}`, {
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
      "communityName": "Ava Chen",
      "communityNumber": "string",
      "congressionalDistrict": "string",
      "county": "string",
      "countyCode": "string",
      "crsRating": "string",
      "id": "string",
      "isCrsCommunity": true,
      "stateAbbreviation": "string",
      "stateNumberCode": "string",
      "subapplicationIdentifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `communityName` | string |  |
| `communityNumber` | string |  |
| `congressionalDistrict` | string |  |
| `county` | string |  |
| `countyCode` | string |  |
| `crsRating` | string |  |
| `id` | string |  |
| `isCrsCommunity` | boolean |  |
| `stateAbbreviation` | string |  |
| `stateNumberCode` | string |  |
| `subapplicationIdentifier` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/HmaSubapplicationsByNfipCrsCommunities` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hma-subapplications-by-nfip-crs-communities.md) for the provider-specific parameters and requirements.

