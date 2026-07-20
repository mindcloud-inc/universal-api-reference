# Supernotes: Get User Sending Email

Retrieves your sending email key from Supernotes.

```
GET https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-user-sending-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supernotes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-user-sending-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supernotes/latest/actions/get-user-sending-email?${params}`, {
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
      "data": "string",
      "enabled": true,
      "expiresWhen": "2026-05-07T12:00:00.000Z",
      "lastUsedWhen": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `enabled` | boolean |  |
| `expiresWhen` | date |  |
| `lastUsedWhen` | date |  |
| `name` | string |  |

## Native endpoint

Through the native Supernotes API, this operation is `GET /keys/email` (base URL `https://api.supernotes.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-sending-email.md) for the provider-specific parameters and requirements.

