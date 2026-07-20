# Trackabi: List Leaves

Retrieves company leave records from Trackabi.

```
GET https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-leaves
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trackabi `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-leaves?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trackabi/latest/actions/list-leaves?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startDate` | date | no | The start date for filtering records in YYYY-MM-DD format. |
| `endDate` | date | no | The end date for filtering records in YYYY-MM-DD format. |
| `own` | number | no | Set to 1 to return only leaves belonging to the API key owner. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "": [
        {
          "cancellationReason": "string",
          "endDate": "string",
          "endDateHalfDay": 1,
          "id": 1,
          "memberId": 1,
          "notes": "string",
          "organizationId": 1,
          "rejectionReason": "string",
          "startDate": "string",
          "startDateHalfDay": 1,
          "status": "string",
          "workingDays": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[].cancellationReason` | string |  |
| `[].endDate` | string |  |
| `[].endDateHalfDay` | number |  |
| `[].id` | number |  |
| `[].memberId` | number |  |
| `[].notes` | string |  |
| `[].organizationId` | number |  |
| `[].rejectionReason` | string |  |
| `[].startDate` | string |  |
| `[].startDateHalfDay` | number |  |
| `[].status` | string |  |
| `[].workingDays` | string |  |

## Native endpoint

Through the native Trackabi API, this operation is `GET /api/v1/leaves` (base URL `https://api.trackabi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leaves.md) for the provider-specific parameters and requirements.

