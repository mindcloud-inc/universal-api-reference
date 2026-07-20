# Strategypoint: List Reports

Retrieves reports from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-reports?${params}`, {
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
      "fileCount": 1,
      "files": [
        {}
      ],
      "format": "string",
      "name": "Ava Chen",
      "periodId": 1,
      "reportId": 1,
      "templateId": 1,
      "zoom": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileCount` | number | The number of generated report files returned. |
| `files` | array<object> | The generated report files. |
| `format` | string | The report output format. |
| `name` | string | The report name. |
| `periodId` | number | The related period identifier. |
| `reportId` | number | The unique report identifier. |
| `templateId` | number | The report template identifier. |
| `zoom` | number | The report zoom setting. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /reports` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reports.md) for the provider-specific parameters and requirements.

