# TeleSign: Get Recordings List By Date Range



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-recordings-list-by-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-recordings-list-by-date-range?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-recordings-list-by-date-range?${params}`, {
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
      "call_recordings": {
        "date": "string",
        "file_name": "Ava Chen",
        "reference_id": "string",
        "status": "string"
      },
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_recordings.date` | string |  |
| `call_recordings.file_name` | string |  |
| `call_recordings.reference_id` | string |  |
| `call_recordings.status` | string |  |
| `token` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `GET /v2/call_recording` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recordings-list-by-date-range.md) for the provider-specific parameters and requirements.

