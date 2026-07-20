# Cloudmersive Document Conversion: Convert Email EML to PDF

Converts an email EML file to PDF.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-eml-to-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Document Conversion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-eml-to-pdf?connectionId=$CONNECTION_ID&inputFile=RnJvbTogU2VuZGVyIDxzZW5kZXJAZXhhbXBsZS5jb20%2BDQpUbzogUmVjaXBpZW50IDxyZWNpcGllbnRAZXhhbXBsZS5jb20%2BDQpEYXRlOiBUdWUsIDA1IE1heSAyMDI2IDEyOjAwOjAwICswMDAwDQpTdWJqZWN0OiBDbG91ZG1lcnNpdmUgU2FtcGxlDQpNZXNzYWdlLUlEOiA8c2FtcGxlLTIwMjYwNTA1QGV4YW1wbGUuY29tPg0KTUlNRS1WZXJzaW9uOiAxLjANCkNvbnRlbnQtVHlwZTogdGV4dC9wbGFpbjsgY2hhcnNldD0idXRmLTgiDQpDb250ZW50LVRyYW5zZmVyLUVuY29kaW5nOiA3Yml0DQoNCkNsb3VkbWVyc2l2ZSBzYW1wbGUgZW1haWwgYm9keS4NCg%3D%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inputFile": "RnJvbTogU2VuZGVyIDxzZW5kZXJAZXhhbXBsZS5jb20+DQpUbzogUmVjaXBpZW50IDxyZWNpcGllbnRAZXhhbXBsZS5jb20+DQpEYXRlOiBUdWUsIDA1IE1heSAyMDI2IDEyOjAwOjAwICswMDAwDQpTdWJqZWN0OiBDbG91ZG1lcnNpdmUgU2FtcGxlDQpNZXNzYWdlLUlEOiA8c2FtcGxlLTIwMjYwNTA1QGV4YW1wbGUuY29tPg0KTUlNRS1WZXJzaW9uOiAxLjANCkNvbnRlbnQtVHlwZTogdGV4dC9wbGFpbjsgY2hhcnNldD0idXRmLTgiDQpDb250ZW50LVRyYW5zZmVyLUVuY29kaW5nOiA3Yml0DQoNCkNsb3VkbWVyc2l2ZSBzYW1wbGUgZW1haWwgYm9keS4NCg=="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDocumentConversion/latest/actions/convert-eml-to-pdf?${params}`, {
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
| `inputFile` | file | yes | Input EML email file to convert to PDF. Default: `RnJvbTogU2VuZGVyIDxzZW5kZXJAZXhhbXBsZS5jb20+DQpUbzogUmVjaXBpZW50IDxyZWNpcGllbnRAZXhhbXBsZS5jb20+DQpEYXRlOiBUdWUsIDA1IE1heSAyMDI2IDEyOjAwOjAwICswMDAwDQpTdWJqZWN0OiBDbG91ZG1lcnNpdmUgU2FtcGxlDQpNZXNzYWdlLUlEOiA8c2FtcGxlLTIwMjYwNTA1QGV4YW1wbGUuY29tPg0KTUlNRS1WZXJzaW9uOiAxLjANCkNvbnRlbnQtVHlwZTogdGV4dC9wbGFpbjsgY2hhcnNldD0idXRmLTgiDQpDb250ZW50LVRyYW5zZmVyLUVuY29kaW5nOiA3Yml0DQoNCkNsb3VkbWVyc2l2ZSBzYW1wbGUgZW1haWwgYm9keS4NCg==`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputFile": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputFile` | string | Converted PDF file content returned by Cloudmersive. |

## Native endpoint

Through the native Cloudmersive Document Conversion API, this operation is `POST /convert/eml/to/pdf` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-eml-to-pdf.md) for the provider-specific parameters and requirements.

