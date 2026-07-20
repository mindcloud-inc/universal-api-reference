# FindyMail: Find Email

Finds a verified email in FindyMail.

```
GET https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FindyMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-email?connectionId=$CONNECTION_ID&name=Elon%20Musk&domain=tesla.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Elon Musk",
  "domain": "tesla.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/findyMail/latest/actions/find-email?${params}`, {
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
| `name` | string | yes | Full name of the person, for example John Doe. Example: `Elon Musk`. |
| `domain` | string | yes | Company domain, for example example.com. Example: `tesla.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "city": "string",
        "company": "string",
        "company_city": "string",
        "company_country": "string",
        "company_region": "string",
        "country": "string",
        "domain": "string",
        "email": "ava@example.com",
        "id": 1,
        "job_title": "string",
        "linkedin_url": "https://example.com",
        "name": "Ava Chen",
        "region": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.city` | string | Contact city. |
| `contact.company` | string | Company name returned for the contact. |
| `contact.company_city` | string | Company city returned for the contact. |
| `contact.company_country` | string | Company country returned for the contact. |
| `contact.company_region` | string | Company region returned for the contact. |
| `contact.country` | string | Contact country. |
| `contact.domain` | string | Company domain returned for the contact. |
| `contact.email` | string | Verified email address returned for the contact, or null when no email is found. |
| `contact.id` | number | FindyMail contact identifier. |
| `contact.job_title` | string | Job title returned for the contact. |
| `contact.linkedin_url` | string | LinkedIn URL returned for the contact. |
| `contact.name` | string | Name returned for the contact. |
| `contact.region` | string | Contact region. |

## Native endpoint

Through the native FindyMail API, this operation is `POST /api/search/name` (base URL `https://app.findymail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

