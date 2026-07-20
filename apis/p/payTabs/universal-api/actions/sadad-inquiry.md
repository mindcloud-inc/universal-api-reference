# PayTabs: Sadad Inquiry



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/sadad-inquiry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/sadad-inquiry?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/sadad-inquiry?${params}`, {
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
      "code": 1,
      "message": "string",
      "paymentResult": {},
      "trace": "string",
      "tranRef": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `paymentResult` | object |  |
| `trace` | string |  |
| `tranRef` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/apm/sadad/ifs/inquiry` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sadad-inquiry.md) for the provider-specific parameters and requirements.

