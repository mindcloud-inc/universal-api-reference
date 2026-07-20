# Timetonic: Get User Session Key

Retrieves a user session key from Timetonic.

```
GET https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-session-key
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetonic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-session-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetonic/latest/actions/get-user-session-key?${params}`, {
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
      "createdVNB": "string",
      "req": "string",
      "sesskey": "string",
      "sstamp": 1,
      "status": "string",
      "transactionId": "string",
      "u_c": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdVNB` | string |  |
| `req` | string |  |
| `sesskey` | string |  |
| `sstamp` | number |  |
| `status` | string |  |
| `transactionId` | string |  |
| `u_c` | string |  |

## Native endpoint

Through the native Timetonic API, this operation is `POST` (base URL `https://timetonic.com/live/api.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-session-key.md) for the provider-specific parameters and requirements.

