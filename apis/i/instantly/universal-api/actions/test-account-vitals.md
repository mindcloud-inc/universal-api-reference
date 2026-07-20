# Instantly: Test Account Vitals

Retrieves account vitals test results from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/test-account-vitals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/test-account-vitals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/test-account-vitals?${params}`, {
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
| `accounts[]` | array<string> | no | Email accounts to test. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email account. |
| `message` | string | Vitals message. |
| `status` | string | Vitals status. |
| `success` | boolean | Whether the vitals check succeeded. |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/accounts/test/vitals` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-account-vitals.md) for the provider-specific parameters and requirements.

