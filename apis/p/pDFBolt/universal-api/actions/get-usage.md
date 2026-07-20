# PDFBolt: Get Usage

Retrieves usage details from PDFBolt.

```
GET https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDFBolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDFBolt/latest/actions/get-usage?${params}`, {
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
      "oneTime": [
        {}
      ],
      "plan": "string",
      "recurring": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `oneTime` | array<object> | One-time usage buckets, when present. |
| `plan` | string | The current PDFBolt subscription plan. |
| `recurring` | array<object> | Recurring usage buckets with remaining quota and expiry. |

## Native endpoint

Through the native PDFBolt API, this operation is `GET /usage` (base URL `https://api.pdfbolt.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

