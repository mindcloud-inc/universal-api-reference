# EmailVerify.io: Find Business Email

Finds a business email in EmailVerify.io by name and domain.

```
GET https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/find-business-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailVerify.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/find-business-email?connectionId=$CONNECTION_ID&name=Ava%20Chen&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/find-business-email?${params}`, {
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
| `name` | string | yes | Person's name to search for on the target domain. |
| `domain` | string | yes | Company domain to search for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Matched or inferred business email address, or null when none is found. |
| `status` | string | Finder result status. |

## Native endpoint

Through the native EmailVerify.io API, this operation is `GET /finder` (base URL `https://app.emailverify.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-business-email.md) for the provider-specific parameters and requirements.

