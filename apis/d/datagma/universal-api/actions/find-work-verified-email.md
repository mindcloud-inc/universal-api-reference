# Datagma: Find Work Verified Email

Finds a verified work email in Datagma.

```
GET https://connect.mindcloud.co/v1/universal/datagma/latest/actions/find-work-verified-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datagma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/find-work-verified-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datagma/latest/actions/find-work-verified-email?${params}`, {
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
| `company_linkedin_slug` | string | no | LinkedIn company URL or company slug used to improve the match rate. |
| `first_name` | string | no | Target person's first name. |
| `last_name` | string | no | Target person's last name. |
| `company` | string | no | Target company name. |
| `linked_in_slug` | string | no | LinkedIn company URL or company slug used to improve the match rate. |
| `find_email_v2_step` | string | no | Use 3 to return the email address or 2 for the domain only; both cost the same. |
| `find_email_v2_country` | string | no | Country hint to improve matching accuracy. Use General if unknown. |
| `full_name` | string | no | Target person's full name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cachAll": true,
      "email": "ava@example.com",
      "emailDomain": "ava@example.com",
      "mxfound": true,
      "patterns": [
        "string"
      ],
      "smtpCheck": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cachAll` | boolean |  |
| `email` | string |  |
| `emailDomain` | string |  |
| `mxfound` | boolean |  |
| `patterns` | array<string> |  |
| `smtpCheck` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Datagma API, this operation is `GET /v8/findEmail` (base URL `https://gateway.datagma.net/api/ingress`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-work-verified-email.md) for the provider-specific parameters and requirements.

