# WellTraq: List Attachments By Upload Date

Retrieves attachments from WellTraq by upload date.

```
GET https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-attachments-by-upload-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WellTraq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-attachments-by-upload-date?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wellTraq/latest/actions/list-attachments-by-upload-date?${params}`, {
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
      "fileName": "Ava Chen",
      "id": "string",
      "uploadDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |
| `id` | string |  |
| `uploadDate` | date |  |

## Native endpoint

Through the native WellTraq API, this operation is `GET /Attachments/ByUploadDate` (base URL `https://welltraq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments-by-upload-date.md) for the provider-specific parameters and requirements.

