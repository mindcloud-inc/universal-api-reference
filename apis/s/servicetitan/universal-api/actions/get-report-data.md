# ServiceTitan: Get Report Data

Retrieves report data from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-report-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-report-data?connectionId=$CONNECTION_ID&limit=25&offset=0&reportCategory=string&reportId=1&parameters%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "reportCategory": "string",
  "reportId": "1",
  "parameters[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-report-data?${params}`, {
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
| `reportCategory` | string | yes | ID of category taken from the category list endpoint. |
| `reportId` | number | yes | ID of report within the category. |
| `parameters[]` | array<object> | yes | List of name/value input parameters for the report. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTotal` | boolean | no | Whether total count should be returned. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST reporting/v2/tenant/{{credentials.tenant}}/report-category/:report_category/reports/:reportId/data` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-report-data.md) for the provider-specific parameters and requirements.

