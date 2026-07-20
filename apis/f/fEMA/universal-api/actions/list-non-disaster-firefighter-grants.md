# FEMA: List Non-Disaster Firefighter Grants

Retrieves non-disaster firefighter grants from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-non-disaster-firefighter-grants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-non-disaster-firefighter-grants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-non-disaster-firefighter-grants?${params}`, {
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
      "awardAmount": 1,
      "awardNumber": "string",
      "fiscalYear": 1,
      "id": "string",
      "programAbbreviation": "string",
      "programName": "Ava Chen",
      "region": 1,
      "vendorName": "Ava Chen",
      "vendorState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `awardAmount` | number |  |
| `awardNumber` | string |  |
| `fiscalYear` | number |  |
| `id` | string |  |
| `programAbbreviation` | string |  |
| `programName` | string |  |
| `region` | number |  |
| `vendorName` | string |  |
| `vendorState` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/NonDisasterAssistanceFirefighterGrants` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-non-disaster-firefighter-grants.md) for the provider-specific parameters and requirements.

