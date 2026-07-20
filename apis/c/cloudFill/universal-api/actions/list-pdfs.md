# CloudFill: List PDFs

Retrieves available PDFs from your CloudFill account.

```
GET https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/list-pdfs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudFill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/list-pdfs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudFill/latest/actions/list-pdfs?${params}`, {
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
      "createdAt": 1,
      "fileName": "Ava Chen",
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Creation time in milliseconds since epoch. |
| `fileName` | string | Stored PDF file name. |
| `key` | string | CloudFill PDF template key. |

## Native endpoint

Through the native CloudFill API, this operation is `GET /api/meta/pdf/` (base URL `https://api.cloudfill.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pdfs.md) for the provider-specific parameters and requirements.

