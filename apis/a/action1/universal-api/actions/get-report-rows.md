# Action1: Get Report Rows

Retrieves report rows from Action1 for a report.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-report-rows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-report-rows?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string",
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-report-rows?${params}`, {
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
| `orgId` | string | yes | Provide an organization ID. |
| `reportId` | string | yes | Provide a specific report ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "drilldown": "string",
      "drilldown_field": "string",
      "fields": "string",
      "group_fields": "string",
      "id": "string",
      "last_refresh": "string",
      "response_type": "string",
      "self": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `drilldown` | string |  |
| `drilldown_field` | string |  |
| `fields` | string |  |
| `group_fields` | string |  |
| `id` | string |  |
| `last_refresh` | string |  |
| `response_type` | string |  |
| `self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /reportdata/:orgId/:reportId/data` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-report-rows.md) for the provider-specific parameters and requirements.

