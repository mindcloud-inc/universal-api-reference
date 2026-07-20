# Quickbase: Run a Report

Runs a Quickbase report and returns its results.

```
GET https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/run-a-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/run-a-report?connectionId=$CONNECTION_ID&tableId=string&reportId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tableId": "string",
  "reportId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/run-a-report?${params}`, {
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
| `tableId` | string | yes | The Quickbase table identifier. |
| `reportId` | string | yes | The Quickbase report identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | The number of rows to skip before returning report results. |
| `top` | number | no | The maximum number of rows to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "fields": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The returned report rows. |
| `fields` | array<object> | Metadata for the report fields. |
| `metadata` | object | Result metadata including counts and pagination values. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/reports/:reportId/run` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-a-report.md) for the provider-specific parameters and requirements.

