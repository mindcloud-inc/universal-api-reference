# US Congress CRS: List CRS Reports

Retrieves CRS reports from US Congress CRS.

```
GET https://connect.mindcloud.co/v1/universal/uSCongressCRS/latest/actions/list-crs-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a US Congress CRS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uSCongressCRS/latest/actions/list-crs-reports?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uSCongressCRS/latest/actions/list-crs-reports?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromDateTime` | date | no | Starting timestamp to filter CRS reports by update date. Use ISO timestamp format such as 2026-01-01T00:00:00Z. |
| `toDateTime` | date | no | Ending timestamp to filter CRS reports by update date. Use ISO timestamp format such as 2026-05-05T00:00:00Z. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CRSReports": [
        {}
      ],
      "pagination": {},
      "request": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CRSReports` | array<object> | CRS report records returned by Congress.gov. |
| `pagination` | object | Pagination metadata including total count and next URL. |
| `request` | object | Request metadata returned by Congress.gov. |

## Native endpoint

Through the native US Congress CRS API, this operation is `GET /crsreport` (base URL `https://api.congress.gov/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crs-reports.md) for the provider-specific parameters and requirements.

