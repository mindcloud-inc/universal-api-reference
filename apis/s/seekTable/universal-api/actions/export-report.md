# SeekTable: Export Report

Exports a SeekTable report in the requested format.

```
GET https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/export-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/export-report?connectionId=$CONNECTION_ID&reportId=b1fcc6be555b4cca91843c86a414da77&format=csv" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reportId": "b1fcc6be555b4cca91843c86a414da77",
  "format": "csv"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/export-report?${params}`, {
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
| `reportId` | string | yes | GUID of the report in your SeekTable account. Example: `b1fcc6be555b4cca91843c86a414da77`. |
| `format` | string | yes | Export format for the generated report file. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Example: `csv`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportParameters` | string | no | JSON object string with report parameter values. Requires Advanced Publishing. Example: `[object Object]`. |
| `htmlInlineStyle` | boolean | no | Enable inline styles in HTML output. |
| `chartOnly` | boolean | no | Render only chart output for pdf or png exports. |
| `valueFormatting` | boolean | no | Whether exported values should use SeekTable value formatting. |
| `rowMode` | string | no | JSON export only: determines whether rows are serialized as arrays or objects. One of: `0`, `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SeekTable API returns.

## Native endpoint

Through the native SeekTable API, this operation is `GET /api/report/:report_id/export` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-report.md) for the provider-specific parameters and requirements.

