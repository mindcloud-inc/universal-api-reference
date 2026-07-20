# Invoice.xhub: Get Spain Formats



```
GET https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-spain-formats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-spain-formats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/get-spain-formats?${params}`, {
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
        {}
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
| `formats` | array<object> |  |
| `name` | string |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `GET /api/v1/invoice/ES/formats` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-spain-formats.md) for the provider-specific parameters and requirements.

