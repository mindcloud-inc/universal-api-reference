# UserCheck: Validate Email

Retrieves email validation details from UserCheck.

```
GET https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/validate-email?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "alias": true,
      "blocklisted": true,
      "did_you_mean": "string",
      "disposable": true,
      "disposable_provider": "string",
      "domain": "string",
      "domain_age_in_days": 1,
      "domain_authority": 1,
      "email": "ava@example.com",
      "mx": true,
      "mx_providers": [
        {}
      ],
      "mx_records": [
        {}
      ],
      "normalized_email": "ava@example.com",
      "public_domain": true,
      "relay_domain": true,
      "role_account": true,
      "spam": true,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alias` | boolean |  |
| `blocklisted` | boolean |  |
| `did_you_mean` | string |  |
| `disposable` | boolean |  |
| `disposable_provider` | string |  |
| `domain` | string |  |
| `domain_age_in_days` | number |  |
| `domain_authority` | number |  |
| `email` | string |  |
| `mx` | boolean |  |
| `mx_providers` | array<object> |  |
| `mx_records` | array<object> |  |
| `normalized_email` | string |  |
| `public_domain` | boolean |  |
| `relay_domain` | boolean |  |
| `role_account` | boolean |  |
| `spam` | boolean |  |
| `status` | number |  |

## Native endpoint

Through the native UserCheck API, this operation is `GET /email/:email` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

