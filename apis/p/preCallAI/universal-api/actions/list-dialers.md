# PreCallAI: List Dialers

Retrieves dialers from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-dialers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-dialers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-dialers?${params}`, {
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
      "data": {
        "auth_token": "string",
        "dialer_type": "string",
        "id": "string",
        "name": "Ava Chen",
        "phone_number": "string",
        "sid": "string"
      },
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of dialers returned by PreCallAI. |
| `data.auth_token` | string | Provider auth token. |
| `data.dialer_type` | string | Dialer provider type. |
| `data.id` | string | Dialer ID. |
| `data.name` | string | Dialer name. |
| `data.phone_number` | string | Dialer phone number. |
| `data.sid` | string | Twilio or provider SID. |
| `message` | string | Provider status message for listing dialers. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the dialer list request succeeded. |

## Native endpoint

Through the native PreCallAI API, this operation is `GET /dialer/list` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dialers.md) for the provider-specific parameters and requirements.

