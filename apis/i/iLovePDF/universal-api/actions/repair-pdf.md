# iLovePDF: Repair PDF

Repairs a PDF in iLovePDF.

```
POST https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/repair-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/repair-pdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/repair-pdf', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "download_filename": "Ava Chen",
      "filesize": 1,
      "output_extensions": [
        "string"
      ],
      "output_filenumber": 1,
      "output_filesize": 1,
      "status": "string",
      "timer": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_filename` | string |  |
| `filesize` | number |  |
| `output_extensions[]` | string |  |
| `output_filenumber` | number |  |
| `output_filesize` | number |  |
| `status` | string |  |
| `timer` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `POST https://:server/v1/process` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/repair-pdf.md) for the provider-specific parameters and requirements.

