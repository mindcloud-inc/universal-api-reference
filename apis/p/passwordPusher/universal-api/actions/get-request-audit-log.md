# Password Pusher: Get Request Audit Log

Retrieves a request audit log from Password Pusher.

```
GET https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/get-request-audit-log
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Password Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/get-request-audit-log?connectionId=$CONNECTION_ID&urlToken=orpw2wkg00vpn0a" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlToken": "orpw2wkg00vpn0a"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passwordPusher/latest/actions/get-request-audit-log?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlToken` | string | yes | The request URL token owned by the authenticated account. Example: `orpw2wkg00vpn0a`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logs": [
        {
          "created_at": "2026-05-07T12:00:00.000Z",
          "ip": "string",
          "kind": "string",
          "referrer": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "user_agent": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logs` | array<object> |  |
| `logs[].created_at` | date |  |
| `logs[].ip` | string |  |
| `logs[].kind` | string |  |
| `logs[].referrer` | string |  |
| `logs[].updated_at` | date |  |
| `logs[].user_agent` | string |  |

## Native endpoint

Through the native Password Pusher API, this operation is `GET /requests/{{urlToken}}/audit` (base URL `https://eu.pwpush.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-request-audit-log.md) for the provider-specific parameters and requirements.

