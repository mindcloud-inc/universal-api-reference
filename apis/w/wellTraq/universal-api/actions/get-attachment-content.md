# WellTraq: Get Attachment Content

Retrieves attachment content from WellTraq.

```
GET https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-attachment-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WellTraq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-attachment-content?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/get-attachment-content?${params}`, {
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
      "chunkSize": 1,
      "content": "string",
      "startIndex": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chunkSize` | number |  |
| `content` | string |  |
| `startIndex` | number |  |

## Native endpoint

Through the native WellTraq API, this operation is `GET /Attachments/GetContent` (base URL `https://welltraq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment-content.md) for the provider-specific parameters and requirements.

