# OpnForm: Export Submissions CSV

Exports form submissions as CSV from OpnForm.

```
GET https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/export-submissions-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpnForm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/export-submissions-csv?connectionId=$CONNECTION_ID&id=1&columns=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "columns": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opnForm/latest/actions/export-submissions-csv?${params}`, {
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
| `id` | number | yes | The numeric ID of the form. |
| `columns` | object | yes | Object mapping field IDs to booleans for the columns to include in the CSV export. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OpnForm API returns.

## Native endpoint

Through the native OpnForm API, this operation is `POST /open/forms/:id/submissions/export` (base URL `https://api.opnform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-submissions-csv.md) for the provider-specific parameters and requirements.

