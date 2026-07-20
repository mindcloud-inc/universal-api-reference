# Company URL Finder: Get Domain by Company Name

Finds a company's domain in Company URL Finder by company name.

```
GET https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/get-domain-by-company-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Company URL Finder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/get-domain-by-company-name?connectionId=$CONNECTION_ID&company_name=Ava%20Chen&country_code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company_name": "Ava Chen",
  "country_code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/get-domain-by-company-name?${params}`, {
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
| `company_name` | string | yes | Company name. |
| `country_code` | string | yes | Two-letter country code. When set, results are limited to that country. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "exists": true,
      "remainingCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | Verified company website domain returned by Company URL Finder. |
| `exists` | boolean | Whether a matching company website domain was found. |
| `remainingCredits` | number | Remaining Company URL Finder credits after the lookup. |

## Native endpoint

Through the native Company URL Finder API, this operation is `POST /v2/services/name_to_domain` (base URL `https://api.companyurlfinder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-by-company-name.md) for the provider-specific parameters and requirements.

