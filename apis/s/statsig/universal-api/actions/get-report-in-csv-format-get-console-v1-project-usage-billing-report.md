# Statsig: Get Report in CSV format

Retrieves a report from Statsig in CSV format.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report?connectionId=$CONNECTION_ID&end=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report?${params}`, {
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
| `end` | number | yes | Unix timestamp in ms |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | number | no | Unix timestamp in ms |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `GET /console/v1/project/usage_billing/report` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-report-in-csv-format-get-console-v1-project-usage-billing-report.md) for the provider-specific parameters and requirements.

