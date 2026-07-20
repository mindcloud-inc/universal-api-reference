# TeleSign: Get Recordings List For A Call



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-recordings-list-for-a-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-recordings-list-for-a-call?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-recordings-list-for-a-call?${params}`, {
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
      "date": "string",
      "file_name": "Ava Chen",
      "reference_id": "string",
      "status": "string",
      "transcribe": {
        "language_code": "string",
        "transcription": [
          {}
        ]
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `file_name` | string |  |
| `reference_id` | string |  |
| `status` | string |  |
| `transcribe.language_code` | string |  |
| `transcribe.transcription` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `GET /v2/call_recording/{reference_id}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recordings-list-for-a-call.md) for the provider-specific parameters and requirements.

