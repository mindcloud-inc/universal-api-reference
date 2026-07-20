# Expensify: Export Reports

Retrieves exported reports from Expensify.

```
GET https://connect.mindcloud.co/v1/universal/expensify/latest/actions/export-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/export-reports?connectionId=$CONNECTION_ID&filtersJson=string&fileExtension=csv&template=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filtersJson": "string",
  "fileExtension": "csv",
  "template": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expensify/latest/actions/export-reports?${params}`, {
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
| `filtersJson` | string | yes | JSON object of combinedReportData filters. |
| `fileExtension` | string | yes | The output file extension. One of: `0`, `1`, `2`, `3`, `4`. Default: `csv`. |
| `template` | string | yes | Freemarker template string used to render the exported report file. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-reports.md) for the provider-specific parameters and requirements.

