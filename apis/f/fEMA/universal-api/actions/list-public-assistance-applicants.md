# FEMA: List Public Assistance Applicants

Retrieves public assistance applicants from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-applicants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-applicants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-public-assistance-applicants?${params}`, {
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
      "addressLine1": "string",
      "addressLine2": "string",
      "applicantId": "string",
      "applicantName": "Ava Chen",
      "city": "string",
      "disasterNumber": 1,
      "hash": "string",
      "id": "string",
      "lastRefresh": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "zipCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `applicantId` | string |  |
| `applicantName` | string |  |
| `city` | string |  |
| `disasterNumber` | number |  |
| `hash` | string |  |
| `id` | string |  |
| `lastRefresh` | date |  |
| `state` | string |  |
| `zipCode` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/PublicAssistanceApplicants` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-public-assistance-applicants.md) for the provider-specific parameters and requirements.

