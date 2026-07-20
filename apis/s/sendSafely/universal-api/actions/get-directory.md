# SendSafely: Get Directory



```
GET https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-directory?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/get-directory?${params}`, {
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
      "directoryId": "string",
      "directoryName": "Ava Chen",
      "files": [
        "string"
      ],
      "response": "string",
      "subDirectories": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directoryId` | string |  |
| `directoryName` | string |  |
| `files` | array<string> |  |
| `response` | string |  |
| `subDirectories` | array<string> |  |

## Native endpoint

Through the native SendSafely API, this operation is `GET /package/:packageId/directory/:directoryId` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-directory.md) for the provider-specific parameters and requirements.

