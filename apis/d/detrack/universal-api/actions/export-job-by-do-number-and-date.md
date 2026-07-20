# Detrack: Export Job By D.O. Number And Date

Exports a job document from Detrack by D.O. number and date.

```
GET https://connect.mindcloud.co/v1/universal/detrack/latest/actions/export-job-by-do-number-and-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/export-job-by-do-number-and-date?connectionId=$CONNECTION_ID&doNumber=string&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "doNumber": "string",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/detrack/latest/actions/export-job-by-do-number-and-date?${params}`, {
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
| `doNumber` | string | yes | D.O. number of the job to export. |
| `date` | string | yes | Job date in YYYY-MM-DD format. |
| `document` | string | no | Document type to export, such as pod or shipping-label. |
| `format` | string | no | Export format, such as pdf or tiff. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Detrack API returns.

## Native endpoint

Through the native Detrack API, this operation is `GET /dn/jobs/export/:do_number/:date` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-job-by-do-number-and-date.md) for the provider-specific parameters and requirements.

