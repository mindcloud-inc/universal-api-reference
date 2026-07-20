# Congress.gov: List Committee Reports

Retrieves committee reports from Congress.gov.

```
GET https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-committee-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Congress.gov `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-committee-reports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/congressgov/latest/actions/list-committee-reports?${params}`, {
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
      "pagination": {},
      "reports": [
        {}
      ],
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object |  |
| `reports` | array<object> |  |
| `request` | object |  |

## Native endpoint

Through the native Congress.gov API, this operation is `GET /committee-report` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-committee-reports.md) for the provider-specific parameters and requirements.

