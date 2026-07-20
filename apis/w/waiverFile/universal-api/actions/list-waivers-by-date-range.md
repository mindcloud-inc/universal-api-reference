# WaiverFile: List Waivers by Date Range

Retrieves waivers from WaiverFile by date range.

```
GET https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waivers-by-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverFile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waivers-by-date-range?connectionId=$CONNECTION_ID&limit=25&offset=0&startDate=2026-05-07T12%3A00%3A00.000Z&endDate=2026-05-07T12%3A00%3A00.000Z&pageIndex=1&pageSize=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "startDate": "2026-05-07T12:00:00.000Z",
  "endDate": "2026-05-07T12:00:00.000Z",
  "pageIndex": "1",
  "pageSize": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverFile/latest/actions/list-waivers-by-date-range?${params}`, {
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
| `startDate` | date | yes |  |
| `endDate` | date | yes |  |
| `pageIndex` | number | yes |  |
| `pageSize` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "?xml": {},
      "ArrayOfWaiver": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `?xml` | object |  |
| `ArrayOfWaiver` | object |  |

## Native endpoint

Through the native WaiverFile API, this operation is `GET /GetAllWaiversByDateRange` (base URL `https://api.waiverfile.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-waivers-by-date-range.md) for the provider-specific parameters and requirements.

