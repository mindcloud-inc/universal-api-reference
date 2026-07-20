# FindyMail: Reverse Email Lookup

Finds contact details in FindyMail by email address.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/reverse-email-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/reverse-email-lookup?connectionId=$CONNECTION_ID&email=john%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "john@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/reverse-email-lookup?${params}`, {
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
| `email` | string | yes | Email address to look up. Example: `john@example.com`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withProfile` | boolean | no | When true, include full profile enrichment; this uses 2 credits instead of 1. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
      "fullName": "Ava Chen",
      "headline": "string",
      "jobTitle": "string",
      "linkedin_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string | Current company name returned when profile enrichment is requested and available. |
| `fullName` | string | Full name returned when profile enrichment is requested and available. |
| `headline` | string | Profile headline returned when profile enrichment is requested and available. |
| `jobTitle` | string | Current job title returned when profile enrichment is requested and available. |
| `linkedin_url` | string | LinkedIn URL found for the email address, or null when none is found. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/search/reverse-email` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-email-lookup.md) for the provider-specific parameters and requirements.

