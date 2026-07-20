# TopMessage: Verify Message Code

Verifies a message code by recipient number in TopMessage.

```
GET https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/verify-message-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TopMessage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/verify-message-code?connectionId=$CONNECTION_ID&to=string&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "to": "string",
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/topMessage/latest/actions/verify-message-code?${params}`, {
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
| `to` | string | yes | The recipient phone number in international format. |
| `code` | string | yes | The verification code to validate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `expired` | boolean | no | When true, include expired verification codes in the lookup. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | The messages that match the verification-code lookup. |
| `pagination` | object | TopMessage pagination metadata when available. |

## Native endpoint

Through the native TopMessage API, this operation is `GET /v1/messages` (base URL `https://api.topmessage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-message-code.md) for the provider-specific parameters and requirements.

