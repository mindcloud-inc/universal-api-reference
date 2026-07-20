# DirectIQ: Get email client report

Retrieves campaign email client details from DirectIQ.

```
GET https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-email-client-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DirectIQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-email-client-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-email-client-report?${params}`, {
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
      "result": [
        [
          {}
        ]
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result[]` | array<object> |  |
| `result[].device` | string |  |
| `result[].email` | string |  |
| `result[].id` | number |  |
| `result[].mailClient` | string |  |
| `result[].openDate` | date |  |
| `result[].openDateOffset` | date |  |
| `result[].openDateString` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native DirectIQ API, this operation is `GET /core/reports/emailclients` (base URL `https://rest.directiq.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-email-client-report.md) for the provider-specific parameters and requirements.

