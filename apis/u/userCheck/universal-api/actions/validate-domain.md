# UserCheck: Validate Domain

Retrieves domain validation details from UserCheck.

```
GET https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/validate-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/validate-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/validate-domain?${params}`, {
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
| `domain` | string | yes | Domain to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocklisted": true,
      "did_you_mean": "string",
      "disposable": true,
      "disposable_provider": "string",
      "domain": "string",
      "domain_age_in_days": 1,
      "domain_authority": 1,
      "mx": true,
      "mx_providers": [
        {}
      ],
      "mx_records": [
        {}
      ],
      "public_domain": true,
      "relay_domain": true,
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
| `blocklisted` | boolean |  |
| `did_you_mean` | string |  |
| `disposable` | boolean |  |
| `disposable_provider` | string |  |
| `domain` | string |  |
| `domain_age_in_days` | number |  |
| `domain_authority` | number |  |
| `mx` | boolean |  |
| `mx_providers` | array<object> |  |
| `mx_records` | array<object> |  |
| `public_domain` | boolean |  |
| `relay_domain` | boolean |  |
| `spam` | boolean |  |
| `status` | number |  |

## Native endpoint

Through the native UserCheck API, this operation is `GET /domain/:domain` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-domain.md) for the provider-specific parameters and requirements.

