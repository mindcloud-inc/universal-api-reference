# Close: List Opportunities

Retrieves opportunities from Close.

```
GET https://connect.mindcloud.co/v1/universal/close/latest/actions/list-opportunities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Close `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/close/latest/actions/list-opportunities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/close/latest/actions/list-opportunities?${params}`, {
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
| `leadId` | string | no | Filter by Lead ID. |
| `query` | string | no | Free-text search query. |
| `statusId` | string | no | Filter by opportunity status ID. |
| `statusType` | string | no | Filter by status type. |
| `userId` | string | no | Filter by owner user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countByValuePeriod": {},
      "data": [
        {}
      ],
      "expectedValueAnnual": 1,
      "expectedValueAnnualFormatted": "string",
      "expectedValueAnnualized": 1,
      "expectedValueAnnualizedFormatted": "string",
      "expectedValueMonthly": 1,
      "expectedValueMonthlyFormatted": "string",
      "expectedValueOneTime": 1,
      "expectedValueOneTimeFormatted": "string",
      "hasMore": true,
      "totalResults": 1,
      "totalValueAnnual": 1,
      "totalValueAnnualFormatted": "string",
      "totalValueAnnualized": 1,
      "totalValueAnnualizedFormatted": "string",
      "totalValueMonthly": 1,
      "totalValueMonthlyFormatted": "string",
      "totalValueOneTime": 1,
      "totalValueOneTimeFormatted": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countByValuePeriod` | object |  |
| `data` | array<object> |  |
| `expectedValueAnnual` | number |  |
| `expectedValueAnnualFormatted` | string |  |
| `expectedValueAnnualized` | number |  |
| `expectedValueAnnualizedFormatted` | string |  |
| `expectedValueMonthly` | number |  |
| `expectedValueMonthlyFormatted` | string |  |
| `expectedValueOneTime` | number |  |
| `expectedValueOneTimeFormatted` | string |  |
| `hasMore` | boolean |  |
| `totalResults` | number |  |
| `totalValueAnnual` | number |  |
| `totalValueAnnualFormatted` | string |  |
| `totalValueAnnualized` | number |  |
| `totalValueAnnualizedFormatted` | string |  |
| `totalValueMonthly` | number |  |
| `totalValueMonthlyFormatted` | string |  |
| `totalValueOneTime` | number |  |
| `totalValueOneTimeFormatted` | string |  |

## Native endpoint

Through the native Close API, this operation is `GET /opportunity/` (base URL `https://api.close.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-opportunities.md) for the provider-specific parameters and requirements.

