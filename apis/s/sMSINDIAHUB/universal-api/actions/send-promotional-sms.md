# SMSINDIAHUB: Send Promotional SMS

Sends a promotional SMS message in SMSINDIAHUB.

```
POST https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send-promotional-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send-promotional-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "msisdn": "string",
  "sid": "string",
  "msg": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSINDIAHUB/latest/actions/send-promotional-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "msisdn": "string",
    "sid": "string",
    "msg": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `msisdn` | string | yes | One or more destination mobile numbers, separated by commas. |
| `sid` | string | yes | The approved sender ID. |
| `msg` | string | yes | The SMS message content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorCode": "string",
      "ErrorMessage": "string",
      "JobId": "string",
      "MessageData": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorCode` | string | Provider result code. |
| `ErrorMessage` | string | Provider result message. |
| `JobId` | string | Provider job identifier. |
| `MessageData` | array<object> | Per-recipient submission details. |

## Native endpoint

Through the native SMSINDIAHUB API, this operation is `GET /vendorsms/pushsms.aspx` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-promotional-sms.md) for the provider-specific parameters and requirements.

