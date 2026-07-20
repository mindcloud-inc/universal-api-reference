# Enrich.so: Cascading ICP People Search

Finds people in Enrich.so by cascading ICP filters.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/cascading-icp-people-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/cascading-icp-people-search?connectionId=$CONNECTION_ID&companyLinkedinUrl=https%3A%2F%2Fwww.linkedin.com%2Fcompany%2Fstripe%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyLinkedinUrl": "https://www.linkedin.com/company/stripe/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/cascading-icp-people-search?${params}`, {
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
| `companyLinkedinUrl` | string | yes | LinkedIn company URL to search. Default: `https://www.linkedin.com/company/stripe/`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cascade[]` | array<object> | no | Optional cascade filter levels. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
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
| `company` | string | Company name. |
| `email` | string | Email address, when included. |
| `firstName` | string | Person first name. |
| `lastName` | string | Person last name. |
| `linkedin` | string | LinkedIn profile URL. |
| `location` | string | Person location. |
| `title` | string | Person job title. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /people-search/waterfall-icp-search` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cascading-icp-people-search.md) for the provider-specific parameters and requirements.

