# ByteForms: Export Responses CSV



```
GET https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/export-responses-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ByteForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/export-responses-csv?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteForms/latest/actions/export-responses-csv?${params}`, {
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
| `formId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ByteForms API returns.

## Native endpoint

Through the native ByteForms API, this operation is `GET /api/form/export/csv/:formId` (base URL `https://api.forms.bytesuite.io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-responses-csv.md) for the provider-specific parameters and requirements.

