# Byteplant Email Validator: Verify Email Address

Retrieves email deliverability details from Byteplant Email Validator.

```
GET https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/verify-email-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Byteplant Email Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/verify-email-address?connectionId=$CONNECTION_ID&emailAddress=name%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailAddress": "name@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/byteplantEmailValidator/latest/actions/verify-email-address?${params}`, {
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
| `emailAddress` | string | yes | Email address to validate. Example: `name@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeout` | number | no | Timeout in seconds (default 10, min 5, max 300). Example: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": "string",
      "freemail": true,
      "info": "string",
      "ratelimitRemain": 1,
      "ratelimitSeconds": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details` | string | Detailed validation status description. |
| `freemail` | boolean | Whether the address uses a freemail provider. |
| `info` | string | Short validation status description. |
| `ratelimitRemain` | number | Remaining requests in the current rate-limit window. |
| `ratelimitSeconds` | number | Seconds remaining in the current rate-limit window. |
| `status` | number | Byteplant validation status code. |

## Native endpoint

Through the native Byteplant Email Validator API, this operation is `GET /api/verify` (base URL `https://api.email-validator.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-address.md) for the provider-specific parameters and requirements.

