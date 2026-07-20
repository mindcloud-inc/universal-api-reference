# TeleSign: Send App Verify Code



```
POST https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/send-app-verify-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/send-app-verify-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/send-app-verify-code', {
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
      "errors": [
        {}
      ],
      "prefix": "string",
      "reference_id": "string",
      "resource_uri": "string",
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      },
      "sub_resource": "string",
      "verify_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Errors returned by TeleSign. |
| `prefix` | string | Caller ID prefix returned by TeleSign. |
| `reference_id` | string | Verification transaction reference ID. |
| `resource_uri` | string | Relative resource URI for the initiated verification. |
| `status.code` | number | Provider status code. |
| `status.description` | string | Provider status description. |
| `status.updated_on` | string | Timestamp when status was last updated. |
| `sub_resource` | string | TeleSign verification sub-resource. |
| `verify_code` | string | Verification code returned by TeleSign. |

## Native endpoint

Through the native TeleSign API, this operation is `POST /v1/verify/auto/voice/initiate` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-app-verify-code.md) for the provider-specific parameters and requirements.

