# Email Verifier Api: Verify Email (GET)



```
GET https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-get
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Email Verifier Api `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-get?connectionId=$CONNECTION_ID&email=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifierApi/latest/actions/verify-email-get?${params}`, {
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
| `email` | string | yes | Email address to verify. Example: `name@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "domain": "string",
      "email": "ava@example.com",
      "emailSuggested": "ava@example.com",
      "error": "string",
      "event": "string",
      "execution": 1,
      "isComplainer": true,
      "isDisposable": true,
      "isFreeService": true,
      "isGibberish": true,
      "isOffensive": true,
      "isRoleAccount": true,
      "mailbox": "string",
      "mxIp": "string",
      "mxLocation": "string",
      "possibleSpamtrap": true,
      "remaining": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string |  |
| `domain` | string |  |
| `email` | string |  |
| `emailSuggested` | string |  |
| `error` | string |  |
| `event` | string |  |
| `execution` | number |  |
| `isComplainer` | boolean |  |
| `isDisposable` | boolean |  |
| `isFreeService` | boolean |  |
| `isGibberish` | boolean |  |
| `isOffensive` | boolean |  |
| `isRoleAccount` | boolean |  |
| `mailbox` | string |  |
| `mxIp` | string |  |
| `mxLocation` | string |  |
| `possibleSpamtrap` | boolean |  |
| `remaining` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Email Verifier Api API, this operation is `GET /v2/` (base URL `https://emailverifierapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-get.md) for the provider-specific parameters and requirements.

