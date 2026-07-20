# FEMA: List HMA Subapplications

Retrieves HMA subapplications from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplications?${params}`, {
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
      "applicantName": "Ava Chen",
      "applicantUei": "string",
      "federalShareAmount": 1,
      "fiscalYear": 1,
      "id": "string",
      "program": "string",
      "region": 1,
      "status": "string",
      "subapplicantCity": "string",
      "subapplicantName": "Ava Chen",
      "subapplicantState": "string",
      "subapplicantStateAbbreviation": "string",
      "subapplicationIdentifier": "string",
      "subapplicationTitle": "string",
      "subapplicationType": "string",
      "totalSubapplicationAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicantName` | string |  |
| `applicantUei` | string |  |
| `federalShareAmount` | number |  |
| `fiscalYear` | number |  |
| `id` | string |  |
| `program` | string |  |
| `region` | number |  |
| `status` | string |  |
| `subapplicantCity` | string |  |
| `subapplicantName` | string |  |
| `subapplicantState` | string |  |
| `subapplicantStateAbbreviation` | string |  |
| `subapplicationIdentifier` | string |  |
| `subapplicationTitle` | string |  |
| `subapplicationType` | string |  |
| `totalSubapplicationAmount` | number |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v2/HmaSubapplications` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hma-subapplications.md) for the provider-specific parameters and requirements.

