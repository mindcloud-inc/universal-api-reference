# MailRook Email Validation: Enrich Email

Retrieves enrichment data from MailRook for an email address.

```
GET https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/enrich-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailRook Email Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/enrich-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailRookEmailValidation/latest/actions/enrich-email?${params}`, {
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
| `email` | string | yes | Email address to enrich. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | MailRook response code. |
| `data` | object | Enrichment result payload from MailRook. |
| `message` | string | MailRook response message. |

## Native endpoint

Through the native MailRook Email Validation API, this operation is `GET /enrich/:email` (base URL `https://api.mailrook.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-email.md) for the provider-specific parameters and requirements.

