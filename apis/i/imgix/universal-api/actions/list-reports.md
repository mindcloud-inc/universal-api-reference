# imgix: List Reports

Retrieves reports from imgix.

```
GET https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a imgix `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/imgix/latest/actions/list-reports?${params}`, {
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
| `pageNumber` | number | no | Zero-indexed page number for report lists. Default: `0`. |
| `pageSize` | number | no | Page size for report lists. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "completed": true,
            "files": [
              "string"
            ],
            "periodEnd": 1,
            "periodStart": 1,
            "reportKey": "string",
            "reportType": "string"
          },
          "id": "string",
          "type": "string"
        }
      ],
      "meta": {
        "pagination": {
          "currentPage": 1,
          "hasNextPage": true,
          "totalRecords": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].attributes.completed` | boolean |  |
| `data[].attributes.files[]` | string |  |
| `data[].attributes.periodEnd` | number |  |
| `data[].attributes.periodStart` | number |  |
| `data[].attributes.reportKey` | string |  |
| `data[].attributes.reportType` | string |  |
| `data[].id` | string |  |
| `data[].type` | string |  |
| `meta.pagination.currentPage` | number |  |
| `meta.pagination.hasNextPage` | boolean |  |
| `meta.pagination.totalRecords` | number |  |

## Native endpoint

Through the native imgix API, this operation is `GET reports` (base URL `https://api.imgix.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

