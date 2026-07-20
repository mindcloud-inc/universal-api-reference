# verifi.email: Validate Email

Validate a single email address and return deliverability checks, including syntax, MX, spoofing, and disposable-provider details.

```
GET https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/validate-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a verifi.email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/validate-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/validate-email?${params}`, {
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
      "details": {
        "disposable": true,
        "mx": {
          "provider": "string",
          "records": [
            "string"
          ]
        },
        "rfcCompliant": true,
        "spoofFree": true,
        "validMxRecord": true
      },
      "email": "ava@example.com",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.disposable` | boolean | Whether the address belongs to a disposable provider. |
| `details.mx.provider` | string | Detected mail provider for the domain. |
| `details.mx.records` | array<string> | Resolved MX records for the domain. |
| `details.rfcCompliant` | boolean | Whether the address matches RFC syntax rules. |
| `details.spoofFree` | boolean | Whether the address appears resistant to spoofing checks. |
| `details.validMxRecord` | boolean | Whether the domain has valid MX records. |
| `email` | string | Email address that was checked. |
| `valid` | boolean | Whether the address appears valid and deliverable. |

## Native endpoint

Through the native verifi.email API, this operation is `GET /check` (base URL `https://api.verifi.email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email.md) for the provider-specific parameters and requirements.

