# FEMA: List NFIP Residential Penetration Rates

Retrieves NFIP residential penetration rates from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-residential-penetration-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-residential-penetration-rates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-nfip-residential-penetration-rates?${params}`, {
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
      "county": "string",
      "fipsCode": "string",
      "id": "string",
      "resContractsInForce": 1,
      "resContractsInForceSfha": 1,
      "resPenetrationRate": 1,
      "resPenetrationRateSfha": 1,
      "state": "string",
      "totalResStructures": 1,
      "totalResStructuresSfha": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asOfDate` | date |  |
| `county` | string |  |
| `fipsCode` | string |  |
| `id` | string |  |
| `resContractsInForce` | number |  |
| `resContractsInForceSfha` | number |  |
| `resPenetrationRate` | number |  |
| `resPenetrationRateSfha` | number |  |
| `state` | string |  |
| `totalResStructures` | number |  |
| `totalResStructuresSfha` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/NfipResidentialPenetrationRates` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-nfip-residential-penetration-rates.md) for the provider-specific parameters and requirements.

