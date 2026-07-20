# Minelead: Validate Email

Validates an email address with Minelead.

```
GET https://connect.mindcloud.co/v1/universal/minelead/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Minelead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minelead/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minelead/latest/actions/validate-email?${params}`, {
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
| `email` | string | yes | Email address to validate. |
| `firstname` | string | no | First name associated with the email. |
| `lastname` | string | no | Last name associated with the email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "exist": true,
      "firstname": "Ava",
      "form": true,
      "lastname": "Chen",
      "mx": true,
      "personal": true,
      "status": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `exist` | boolean |  |
| `firstname` | string |  |
| `form` | boolean |  |
| `lastname` | string |  |
| `mx` | boolean |  |
| `personal` | boolean |  |
| `status` | string |  |
| `timestamp` | number |  |

## Native endpoint

Through the native Minelead API, this operation is `GET /validate` (base URL `https://api.minelead.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

