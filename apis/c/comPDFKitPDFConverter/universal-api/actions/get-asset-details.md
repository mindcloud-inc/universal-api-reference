# ComPDFKit PDF Converter: Get Asset Details

Retrieves processed asset details from ComPDFKit PDF Converter.

```
GET https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/get-asset-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ComPDFKit PDF Converter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/get-asset-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comPDFKitPDFConverter/latest/actions/get-asset-details?${params}`, {
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
      "data": {},
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
| `data` | object |  |
| `msg` | string |  |

## Native endpoint

Through the native ComPDFKit PDF Converter API, this operation is `GET /v2/asset/info` (base URL `https://api-server.compdf.com/server`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-details.md) for the provider-specific parameters and requirements.

