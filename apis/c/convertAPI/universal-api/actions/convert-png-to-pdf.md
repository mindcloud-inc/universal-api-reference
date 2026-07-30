# ConvertAPI: Convert PNG to PDF

Converts a PNG file to PDF with ConvertAPI.

```
POST https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/convert-png-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConvertAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/convert-png-to-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/convertAPI/latest/actions/convert-png-to-pdf', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parameters[].FileValue.Name` | string | no | The current name of the file. |
| `parameters[].Name` | string | no | Default: `File`. |
| `storeFile` | boolean | no | When the `StoreFile` parameter is set to `True`, your converted file is written to ConvertAPI’s encrypted, temporary storage and made available via a time-limited secure download URL, valid for up to 3 hours. After this period, the file is permanently deleted. When `StoreFile` is set to `False`, conversion happens entirely in-memory. The raw file bytes are streamed back in the API response without touching disk or external storage, ensuring maximum security and zero persistence so that only you can access the content. |
| `parameters[].FileValue` | object | no |  |
| `parameters[].FileValue.Data` | string | no | A base64 encoded string of your png image - or an image url. |
| `pdfa` | boolean | no | Create PDF/A-1b compliant document. |
| `parameters[]` | array<object> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConvertAPI API returns.

## Native endpoint

Through the native ConvertAPI API, this operation is `POST /convert/png/to/pdf` (base URL `https://v2.convertapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-png-to-pdf.md) for the provider-specific parameters and requirements.

