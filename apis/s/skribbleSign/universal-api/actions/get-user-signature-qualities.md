# Skribble Sign: Get User Signature Qualities

Retrieves user signature qualities from Skribble Sign.

```
GET https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-user-signature-qualities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-user-signature-qualities?connectionId=$CONNECTION_ID&username=%7B%7Bcredentials.username%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "{{credentials.username}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/get-user-signature-qualities?${params}`, {
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
| `username` | string | yes | The Skribble username to inspect. Default: `{{credentials.username}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aes": {},
      "aes_minimal": {},
      "qes": {},
      "ses": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aes` | object | AES availability bucket. |
| `aes_minimal` | object | AES minimal availability bucket. |
| `qes` | object | QES availability bucket. |
| `ses` | object | SES availability bucket. |

## Native endpoint

Through the native Skribble Sign API, this operation is `GET /v2/user/signature-qualities` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-signature-qualities.md) for the provider-specific parameters and requirements.

