# Ideal Postcodes: Email Validation

Validates an email address in Ideal Postcodes.

```
GET https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/email-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ideal Postcodes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/email-validation?connectionId=$CONNECTION_ID&query=foo%40domain.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "foo@domain.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/idealPostcodes/latest/actions/email-validation?${params}`, {
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
| `query` | string | yes | Email address to validate. Default: `foo@domain.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags` | string | no | Comma-separated tags to associate with the validation request. |

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
| `catchall` | boolean |  |
| `deliverable` | boolean |  |
| `disposable` | boolean |  |
| `free` | boolean |  |
| `result` | string |  |
| `role` | boolean |  |
| `suggestions[]` | string |  |

## Native endpoint

Through the native Ideal Postcodes API, this operation is `GET /emails` (base URL `https://api.ideal-postcodes.co.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/email-validation.md) for the provider-specific parameters and requirements.

