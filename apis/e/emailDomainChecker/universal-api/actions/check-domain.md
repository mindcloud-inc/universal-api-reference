# Email Domain Checker: Check Domain



```
GET https://connect.mindcloud.co/v1/universal/emailDomainChecker/latest/actions/check-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Email Domain Checker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailDomainChecker/latest/actions/check-domain?connectionId=$CONNECTION_ID&domain=mightora.io" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "mightora.io"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailDomainChecker/latest/actions/check-domain?${params}`, {
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
| `domain` | string | yes | Email address or email domain to check. Defaults to mightora.io for a reliable scaffold test. Default: `mightora.io`. Example: `mightora.io`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email_delivered_to": "ava@example.com",
      "email_delivered_to_array": [
        "ava@example.com"
      ],
      "message": "string",
      "message_from_developer": "string",
      "more_info": "https://example.com",
      "valid_email_domain": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email_delivered_to` | string | Mail server where email for the domain will be delivered. |
| `email_delivered_to_array` | array<string> | Mail servers where email for the domain will be delivered. |
| `message` | string | Human-readable result message from the email checker. |
| `message_from_developer` | string | Message from the developer about the platform or API. |
| `more_info` | string | More information link for the tool. |
| `valid_email_domain` | boolean | Whether the email domain is valid. |

## Native endpoint

Through the native Email Domain Checker API, this operation is `GET /checkDomain/` (base URL `https://api.mightora.io/emailDomainChecker`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain.md) for the provider-specific parameters and requirements.

