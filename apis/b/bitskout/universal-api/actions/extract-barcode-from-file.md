# Bitskout: Extract Barcode from File

Extracts barcode values from a file with Bitskout.

```
POST https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-barcode-from-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitskout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-barcode-from-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitskout/latest/actions/extract-barcode-from-file', {
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
| `fileUrl` | string | no | Direct download URL for the file that contains a barcode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputs": {
        "barcode": "string",
        "RawJSON": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputs` | object | Barcode extraction outputs |
| `outputs.barcode` | string | Barcode value |
| `outputs.RawJSON` | string | Raw JSON |

## Native endpoint

Through the native Bitskout API, this operation is `POST /actions/barcodes` (base URL `https://api.bitskout.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-barcode-from-file.md) for the provider-specific parameters and requirements.

