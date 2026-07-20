# SMSINDIAHUB (India): Send Transactional SMS



```
POST https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/send-transactional-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSINDIAHUB (India) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/send-transactional-sms" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSINDIAHUBIndia/latest/actions/send-transactional-sms', {
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
| `msisdn` | string | yes | Single recipient number or a comma-separated list of up to 100 numbers. |
| `sid` | string | yes | Approved sender ID. |
| `msg` | string | yes | SMS message text. |

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

Through the native SMSINDIAHUB (India) API, this operation is `GET /vendorsms/pushsms.aspx` (base URL `https://cloud.smsindiahub.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-transactional-sms.md) for the provider-specific parameters and requirements.

