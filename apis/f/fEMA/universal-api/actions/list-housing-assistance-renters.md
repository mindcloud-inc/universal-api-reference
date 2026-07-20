# FEMA: List Housing Assistance Renters

Retrieves housing assistance renter records from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-housing-assistance-renters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-housing-assistance-renters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-housing-assistance-renters?${params}`, {
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
      "approvedForFemaAssistance": 1,
      "city": "string",
      "county": "string",
      "disasterNumber": 1,
      "id": "string",
      "otherNeedsAmount": 1,
      "rentalAmount": 1,
      "repairReplaceAmount": 1,
      "state": "string",
      "totalApprovedIhpAmount": 1,
      "totalInspected": 1,
      "totalInspectedWithNoDamage": 1,
      "totalWithMajorDamage": 1,
      "totalWithModerateDamage": 1,
      "totalWithSubstantialDamage": 1,
      "validRegistrations": 1,
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvedForFemaAssistance` | number |  |
| `city` | string |  |
| `county` | string |  |
| `disasterNumber` | number |  |
| `id` | string |  |
| `otherNeedsAmount` | number |  |
| `rentalAmount` | number |  |
| `repairReplaceAmount` | number |  |
| `state` | string |  |
| `totalApprovedIhpAmount` | number |  |
| `totalInspected` | number |  |
| `totalInspectedWithNoDamage` | number |  |
| `totalWithMajorDamage` | number |  |
| `totalWithModerateDamage` | number |  |
| `totalWithSubstantialDamage` | number |  |
| `validRegistrations` | number |  |
| `zipCode` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/HousingAssistanceRenters` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-housing-assistance-renters.md) for the provider-specific parameters and requirements.

