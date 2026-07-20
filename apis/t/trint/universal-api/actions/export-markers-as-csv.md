# Trint: Export Markers as CSV

Exports file markers as CSV from Trint.

```
GET https://connect.mindcloud.co/v1/universal/trint/latest/actions/export-markers-as-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trint/latest/actions/export-markers-as-csv?connectionId=$CONNECTION_ID&trintId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trintId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trint/latest/actions/export-markers-as-csv?${params}`, {
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
| `trintId` | string | yes | The Trint file identifier to export. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `title` | string | Exported asset title. |
| `url` | string | Temporary download URL for the exported asset. |

## Native endpoint

Through the native Trint API, this operation is `GET /export/csv/markers/:trintId` (base URL `https://api.trint.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-markers-as-csv.md) for the provider-specific parameters and requirements.

