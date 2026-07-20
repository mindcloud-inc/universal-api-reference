# Enrich.so: Find a Professional Email

Finds a professional email in Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-professional-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-professional-email?connectionId=$CONNECTION_ID&firstName=Sarah&lastName=Chen&domain=stripe.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "firstName": "Sarah",
  "lastName": "Chen",
  "domain": "stripe.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-professional-email?${params}`, {
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
| `firstName` | string | yes | Person first name. Default: `Sarah`. |
| `lastName` | string | yes | Person last name. Default: `Chen`. |
| `domain` | string | yes | Company domain. Default: `stripe.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept_all": true,
      "confidence": "string",
      "credits_remaining": 1,
      "credits_used": 1,
      "domain": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "found": true,
      "lastName": "Chen",
      "message": "string",
      "success": true,
      "total_credits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accept_all` | boolean | Whether the domain is configured as accept-all. |
| `confidence` | string | Confidence for the resolved email. |
| `credits_remaining` | number | Credits remaining after the request. |
| `credits_used` | number | Credits consumed by the request. |
| `domain` | string | Company domain used for the lookup. |
| `email` | string | Resolved work email address. |
| `firstName` | string | First name returned by Enrich. |
| `found` | boolean | Whether an email record was found. |
| `lastName` | string | Last name returned by Enrich. |
| `message` | string | Provider status message for the lookup. |
| `success` | boolean | Whether the email lookup request succeeded. |
| `total_credits` | number | Total credits available to the account. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /email-finder` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-professional-email.md) for the provider-specific parameters and requirements.

