# TeleSign: Check Phone Number Channel Capability



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-channel-capability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-channel-capability?connectionId=$CONNECTION_ID&channel=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "phoneNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/check-phone-number-channel-capability?${params}`, {
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
| `channel` | string | yes | The messaging channel to evaluate for the phone number. |
| `phoneNumber` | string | yes | The destination phone number in E.164 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reference_id` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `GET /capability/{channel}/{phone_number}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-phone-number-channel-capability.md) for the provider-specific parameters and requirements.

