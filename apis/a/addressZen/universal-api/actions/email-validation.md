# AddressZen: Email Validation

Retrieves email validation details from AddressZen.

```
GET https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/email-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddressZen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/email-validation?connectionId=$CONNECTION_ID&query=test%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "test@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressZen/latest/actions/email-validation?${params}`, {
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
| `query` | string | yes | Email address to validate Example: `test@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "catchall": true,
      "deliverable": true,
      "disposable": true,
      "free": true,
      "result": "string",
      "role": true,
      "suggestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `catchall` | boolean | Whether the domain is catch-all |
| `deliverable` | boolean | Whether the email appears deliverable |
| `disposable` | boolean | Whether the address appears disposable |
| `free` | boolean | Whether the address uses a free provider |
| `result` | string | Email deliverability classification |
| `role` | boolean | Whether the address appears role-based |
| `suggestions` | array<string> | Suggested alternate email values |

## Native endpoint

Through the native AddressZen API, this operation is `GET /emails` (base URL `https://api.addresszen.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-validation.md) for the provider-specific parameters and requirements.

