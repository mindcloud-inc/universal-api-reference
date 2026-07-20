# Sniffmail: Validate Credentials

Validates Sniffmail credentials with a test email verification request.

```
GET https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/validate-credentials
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sniffmail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/validate-credentials?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sniffmail/latest/actions/validate-credentials?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "is_deliverable": true,
      "is_disposable": true,
      "is_reachable": "string",
      "is_role_account": true,
      "is_valid": true,
      "mx_valid": true,
      "reason": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | The fixed sample email used for connection validation. |
| `is_deliverable` | boolean | Whether the sample mailbox appears deliverable. |
| `is_disposable` | boolean | Whether the sample address belongs to a disposable email provider. |
| `is_reachable` | string | Sniffmail reachability classification for the sample email address. |
| `is_role_account` | boolean | Whether the sample address is a role inbox such as support@ or info@. |
| `is_valid` | boolean | Whether Sniffmail considers the sample address valid overall. |
| `mx_valid` | boolean | Whether the sample domain has valid MX records. |
| `reason` | string | Human-readable verification result reason. |

## Native endpoint

Through the native Sniffmail API, this operation is `POST /verify` (base URL `https://api.sniffmail.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-credentials.md) for the provider-specific parameters and requirements.

