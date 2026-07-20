# ComPDFKit PDF Converter: List Supported PDF Tools

Retrieves supported PDF tools from ComPDFKit PDF Converter.

```
GET https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/list-supported-pdf-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComPDFKit PDF Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/list-supported-pdf-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/list-supported-pdf-tools?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": [
        {}
      ],
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `data` | array<object> |  |
| `msg` | string |  |

## Native endpoint

Through the native ComPDFKit PDF Converter API, this operation is `GET /v2/tool/support` (base URL `https://api-server.compdf.com/server`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-pdf-tools.md) for the provider-specific parameters and requirements.

