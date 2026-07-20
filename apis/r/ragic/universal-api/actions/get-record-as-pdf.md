# Ragic: Get Record As PDF

Retrieves a record as PDF from Ragic.

```
GET https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-record-as-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-record-as-pdf?connectionId=$CONNECTION_ID&tabFolderPath=ragic-setup&sheetIndex=8&recordId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8",
  "recordId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-record-as-pdf?${params}`, {
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
| `tabFolderPath` | string | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. Default: `ragic-setup`. |
| `sheetIndex` | number | yes | Numeric sheet identifier from the target Ragic resource URL. Default: `8`. |
| `recordId` | number | yes | Numeric record ID from the target Ragic record URL. Default: `0`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ragic API returns.

## Native endpoint

Through the native Ragic API, this operation is `GET /:tabFolderPath/:sheetIndex/:recordId.pdf` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-record-as-pdf.md) for the provider-specific parameters and requirements.

