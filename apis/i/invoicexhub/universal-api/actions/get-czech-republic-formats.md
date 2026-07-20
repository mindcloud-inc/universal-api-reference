# Invoice.xhub: Get Czech Republic Formats



```
GET https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-czech-republic-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-czech-republic-formats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-czech-republic-formats?${params}`, {
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
      "formats": [
        "string"
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `formats` | array<string> |  |
| `name` | string |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `GET /api/v1/invoice/CZ/formats` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-czech-republic-formats.md) for the provider-specific parameters and requirements.

