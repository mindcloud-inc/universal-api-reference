# ServiceTitan: Get Report

Retrieves a report definition from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-report?connectionId=$CONNECTION_ID&reportCategory=string&reportId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportCategory": "string",
  "reportId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-report?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "dataType": "string",
      "label": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dataType` | string | Report field data type. |
| `label` | string | Report field display label. |
| `name` | string | Report field API name. |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET reporting/v2/tenant/{{credentials.tenant}}/report-category/:report_category/reports/:reportId` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

