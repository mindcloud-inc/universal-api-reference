# Skribble: Get User Signature Qualities Detail

Retrieves detailed user signature qualities from Skribble.

```
GET https://connect.mindcloud.co/v1/universal/skribble/latest/actions/get-user-signature-qualities-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/get-user-signature-qualities-detail?connectionId=$CONNECTION_ID&username=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribble/latest/actions/get-user-signature-qualities-detail?${params}`, {
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
| `username` | string | yes | The Skribble username to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aes": {},
      "aes_minimal": {},
      "demo": {},
      "part11": {},
      "qes": {},
      "seal": {},
      "ses": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aes` | object | Detailed quality result bucket for AES. |
| `aes_minimal` | object | Detailed quality result bucket for AES minimal. |
| `demo` | object | Demo signing quality details. |
| `part11` | object | Part 11 signing quality details. |
| `qes` | object | Detailed quality result bucket for QES. |
| `seal` | object | Seal signing quality details. |
| `ses` | object | Detailed quality result bucket for SES. |

## Native endpoint

Through the native Skribble API, this operation is `GET /v2/user/signature-qualities-detail` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-signature-qualities-detail.md) for the provider-specific parameters and requirements.

