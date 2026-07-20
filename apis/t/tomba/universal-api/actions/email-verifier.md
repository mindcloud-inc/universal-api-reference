# Tomba: Email Verifier

Verifies an email address in Tomba.

```
GET https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-verifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tomba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-verifier?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tomba/latest/actions/email-verifier?${params}`, {
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
| `email` | string | yes | Email address to verify. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `enrichMobile` | boolean | no | Include phone data when available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": {
        "accept_all": true,
        "disposable": true,
        "email": "ava@example.com",
        "result": "ava@example.com",
        "score": 1,
        "status": "ava@example.com"
      },
      "sources": [
        {
          "uri": "string"
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
| `email.accept_all` | boolean |  |
| `email.disposable` | boolean |  |
| `email.email` | string |  |
| `email.result` | string |  |
| `email.score` | number |  |
| `email.status` | string |  |
| `sources[].uri` | string |  |

## Native endpoint

Through the native Tomba API, this operation is `GET /email-verifier` (base URL `https://api.tomba.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-verifier.md) for the provider-specific parameters and requirements.

