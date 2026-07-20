# FEMA: List NFIP Community Layer Comprehensive

Retrieves NFIP community layer records from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-community-layer-comprehensive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-community-layer-comprehensive?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-community-layer-comprehensive?${params}`, {
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
      "alternateName": "Ava Chen",
      "censusGeoid": "string",
      "censusHousingUnitsEntire": 1,
      "censusPopulationEntire": 1,
      "censusYear": 1,
      "communityIdNumber": "string",
      "communityName": "Ava Chen",
      "communityNameShort": "Ava Chen",
      "county": "string",
      "countyCode": "string",
      "id": 1,
      "landAreaEntire": 1,
      "layerTypeCode": "string",
      "stateCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternateName` | string |  |
| `censusGeoid` | string |  |
| `censusHousingUnitsEntire` | number |  |
| `censusPopulationEntire` | number |  |
| `censusYear` | number |  |
| `communityIdNumber` | string |  |
| `communityName` | string |  |
| `communityNameShort` | string |  |
| `county` | string |  |
| `countyCode` | string |  |
| `id` | number |  |
| `landAreaEntire` | number |  |
| `layerTypeCode` | string |  |
| `stateCode` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/NfipCommunityLayerComprehensive` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfip-community-layer-comprehensive.md) for the provider-specific parameters and requirements.

