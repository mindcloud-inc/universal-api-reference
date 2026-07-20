# ClearBounce: Verify Email

Verifies a single email address in ClearBounce.

```
GET https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/verify-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClearBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/verify-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearBounce/latest/actions/verify-email?${params}`, {
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
| `email` | string | yes | The email address to verify with ClearBounce. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsRemaining": 1,
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsRemaining` | number | Remaining ClearBounce credits after the request. |
| `data` | object | Verification result for the requested email address. |
| `success` | boolean | Whether the ClearBounce verification request succeeded. |

## Native endpoint

Through the native ClearBounce API, this operation is `POST /verify` (base URL `https://api.clearbounce.net/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email.md) for the provider-specific parameters and requirements.

