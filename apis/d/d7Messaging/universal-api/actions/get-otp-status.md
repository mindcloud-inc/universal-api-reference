# D7 Messaging: Get OTP Status

Retrieves OTP status from D7 Messaging.

```
GET https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-otp-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a D7 Messaging `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-otp-status?connectionId=$CONNECTION_ID&otpId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "otpId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/d7Messaging/latest/actions/get-otp-status?${params}`, {
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
| `otpId` | string | yes | OTP ID returned by Send OTP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native D7 Messaging API, this operation is `GET /verify/v1/report/:otp_id` (base URL `https://api.d7networks.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-otp-status.md) for the provider-specific parameters and requirements.

