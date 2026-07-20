# DynamicPDF: Merge PDFs

Merges PDFs in DynamicPDF API.

```
POST https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/merge-pdfs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/merge-pdfs" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "instructions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/merge-pdfs', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "instructions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `instructions` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number | Generated PDF bytes returned by DynamicPDF. |
| `type` | string | Raw response wrapper type for the generated PDF content. |

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/pdf` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-pdfs.md) for the provider-specific parameters and requirements.

