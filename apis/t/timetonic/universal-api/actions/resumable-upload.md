# Timetonic: Resumable Upload

Creates a resumable upload in Timetonic.

```
POST https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/resumable-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/resumable-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/resumable-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "createdVNB": "string",
      "errorCode": "string",
      "errorMsg": "string",
      "req": "string",
      "status": "string",
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string |  |
| `errorCode` | string |  |
| `errorMsg` | string |  |
| `req` | string |  |
| `status` | string |  |
| `transactionId` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/resumable-upload.md) for the provider-specific parameters and requirements.

