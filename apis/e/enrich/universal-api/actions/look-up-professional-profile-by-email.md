# Enrich.so: Look Up a Professional Profile by Email

Retrieves a professional profile by email from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/look-up-professional-profile-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/look-up-professional-profile-by-email?connectionId=$CONNECTION_ID&email=sarah.chen%40stripe.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "sarah.chen@stripe.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/look-up-professional-profile-by-email?${params}`, {
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
| `email` | string | yes | Email address to look up. Default: `sarah.chen@stripe.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "lastName": "Chen",
      "linkedin": "https://example.com",
      "location": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string | Current company name. |
| `email` | string | Email address used for the lookup. |
| `firstName` | string | Person first name. |
| `fullName` | string | Person full name. |
| `lastName` | string | Person last name. |
| `linkedin` | string | LinkedIn profile URL. |
| `location` | string | Person location. |
| `title` | string | Current job title. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /reverse-lookup/lookup` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/look-up-professional-profile-by-email.md) for the provider-specific parameters and requirements.

