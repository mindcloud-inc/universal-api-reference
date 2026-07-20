# DynamicPDF: Get PDF XMP Metadata

Retrieves PDF XMP metadata from DynamicPDF API.

```
GET https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/get-pdf-xmp-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DynamicPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/get-pdf-xmp-metadata?connectionId=$CONNECTION_ID&pdf=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pdf": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicPDFAPI/latest/actions/get-pdf-xmp-metadata?${params}`, {
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
| `pdf` | file | yes | PDF file sent as the raw request body. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DynamicPDF API returns.

## Native endpoint

Through the native DynamicPDF API, this operation is `POST /v1.0/pdf-xmp` (base URL `https://api.dpdf.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pdf-xmp-metadata.md) for the provider-specific parameters and requirements.

