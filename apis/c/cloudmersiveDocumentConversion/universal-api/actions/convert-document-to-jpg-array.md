# Cloudmersive Document Conversion: Convert Document to JPG Array

Converts a document to JPG images in Cloudmersive Document Conversion.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-document-to-jpg-array
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Document Conversion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-document-to-jpg-array?connectionId=$CONNECTION_ID&inputFile=JVBERi0xLjQKMSAwIG9iaiA8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4gZW5kb2JqCjIgMCBvYmogPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4gZW5kb2JqCjMgMCBvYmogPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCAyMDAgMjAwXSAvQ29udGVudHMgNCAwIFIgPj4gZW5kb2JqCjQgMCBvYmogPDwgL0xlbmd0aCA0NCA%2BPiBzdHJlYW0KQlQgL0YxIDEyIFRmIDIwIDEwMCBUZCAoQ2xvdWRtZXJzaXZlIHNhbXBsZSBQREYpIFRqIEVUCmVuZHN0cmVhbSBlbmRvYmoKeHJlZgowIDUKMDAwMDAwMDAwMCA2NTUzNSBmIAp0cmFpbGVyIDw8IC9Sb290IDEgMCBSIC9TaXplIDUgPj4Kc3RhcnR4cmVmCjAKJSVFT0YK" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputFile": "JVBERi0xLjQKMSAwIG9iaiA8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4gZW5kb2JqCjIgMCBvYmogPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4gZW5kb2JqCjMgMCBvYmogPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCAyMDAgMjAwXSAvQ29udGVudHMgNCAwIFIgPj4gZW5kb2JqCjQgMCBvYmogPDwgL0xlbmd0aCA0NCA+PiBzdHJlYW0KQlQgL0YxIDEyIFRmIDIwIDEwMCBUZCAoQ2xvdWRtZXJzaXZlIHNhbXBsZSBQREYpIFRqIEVUCmVuZHN0cmVhbSBlbmRvYmoKeHJlZgowIDUKMDAwMDAwMDAwMCA2NTUzNSBmIAp0cmFpbGVyIDw8IC9Sb290IDEgMCBSIC9TaXplIDUgPj4Kc3RhcnR4cmVmCjAKJSVFT0YK"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-document-to-jpg-array?${params}`, {
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
| `inputFile` | file | yes | Input file to automatically detect and convert to JPG pages. Default: `JVBERi0xLjQKMSAwIG9iaiA8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4gZW5kb2JqCjIgMCBvYmogPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4gZW5kb2JqCjMgMCBvYmogPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvTWVkaWFCb3ggWzAgMCAyMDAgMjAwXSAvQ29udGVudHMgNCAwIFIgPj4gZW5kb2JqCjQgMCBvYmogPDwgL0xlbmd0aCA0NCA+PiBzdHJlYW0KQlQgL0YxIDEyIFRmIDIwIDEwMCBUZCAoQ2xvdWRtZXJzaXZlIHNhbXBsZSBQREYpIFRqIEVUCmVuZHN0cmVhbSBlbmRvYmoKeHJlZgowIDUKMDAwMDAwMDAwMCA2NTUzNSBmIAp0cmFpbGVyIDw8IC9Sb290IDEgMCBSIC9TaXplIDUgPj4Kc3RhcnR4cmVmCjAKJSVFT0YK`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "JpgResultPages": [
        {}
      ],
      "Successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `JpgResultPages` | array<object> | Array of converted JPG page results with PageNumber and Content. |
| `Successful` | boolean | True if the operation was successful. |

## Native endpoint

Through the native Cloudmersive Document Conversion API, this operation is `POST /convert/autodetect/to/jpg` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-document-to-jpg-array.md) for the provider-specific parameters and requirements.

