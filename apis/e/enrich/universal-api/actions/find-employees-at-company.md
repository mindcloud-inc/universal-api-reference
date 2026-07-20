# Enrich.so: Find Employees At A Company

Finds company employees in Enrich.so by LinkedIn URL.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-employees-at-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-employees-at-company?connectionId=$CONNECTION_ID&companyLinkedinUrl=https%3A%2F%2Fwww.linkedin.com%2Fcompany%2Fstripe%2F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyLinkedinUrl": "https://www.linkedin.com/company/stripe/"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/find-employees-at-company?${params}`, {
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
| `country[]` | array<string> | no | Optional country filters. |
| `maxResults` | number | no | Results per page, 1-100. |
| `page` | number | no | Page number, starting at 1. |

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
| `email` | string | Employee email, when included. |
| `firstName` | string | Employee first name. |
| `lastName` | string | Employee last name. |
| `linkedin` | string | Employee LinkedIn profile URL. |
| `location` | string | Employee location. |
| `title` | string | Employee job title. |

## Native endpoint

Through the native Enrich.so API, this operation is `POST /people-search/employee-finder` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-employees-at-company.md) for the provider-specific parameters and requirements.

