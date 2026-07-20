# Strategypoint: Get Report

Retrieves a report from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-report?connectionId=$CONNECTION_ID&reportId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/get-report?${params}`, {
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
| `reportId` | number | yes | The unique report identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "format": "string",
      "name": "Ava Chen",
      "periodId": 1,
      "reportId": 1,
      "templateId": 1,
      "viewportWidth": 1,
      "zipOnly": true,
      "zoom": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `format` | string | The report output format. |
| `name` | string | The report name. |
| `periodId` | number | The related period identifier. |
| `reportId` | number | The unique report identifier. |
| `templateId` | number | The report template identifier. |
| `viewportWidth` | number | The viewport width used for report rendering. |
| `zipOnly` | boolean | Whether the report is delivered only as a zip file. |
| `zoom` | number | The report zoom setting. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /reports/{reportId}` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report.md) for the provider-specific parameters and requirements.

