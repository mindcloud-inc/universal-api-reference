# mails.so: Validate Email

Retrieves email validation results from mails.so.

```
GET https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mails.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=user%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "user@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailsso/latest/actions/validate-email?${params}`, {
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
| `email` | string | yes | Email address to validate Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "didYouMean": "string",
      "domain": "string",
      "email": "ava@example.com",
      "id": "string",
      "isDisposable": true,
      "isFree": true,
      "isvDomain": true,
      "isvFormat": true,
      "isvMx": true,
      "isvNoblock": true,
      "isvNocatchall": true,
      "isvNogeneric": true,
      "mxRecord": "string",
      "provider": "string",
      "reason": "string",
      "result": "string",
      "score": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `didYouMean` | string |  |
| `domain` | string |  |
| `email` | string |  |
| `id` | string |  |
| `isDisposable` | boolean |  |
| `isFree` | boolean |  |
| `isvDomain` | boolean |  |
| `isvFormat` | boolean |  |
| `isvMx` | boolean |  |
| `isvNoblock` | boolean |  |
| `isvNocatchall` | boolean |  |
| `isvNogeneric` | boolean |  |
| `mxRecord` | string |  |
| `provider` | string |  |
| `reason` | string |  |
| `result` | string |  |
| `score` | number |  |
| `username` | string |  |

## Native endpoint

Through the native mails.so API, this operation is `GET /validate` (base URL `https://api.mails.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

