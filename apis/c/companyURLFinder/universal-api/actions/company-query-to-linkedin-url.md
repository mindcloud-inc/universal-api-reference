# Company URL Finder: Company Query to LinkedIn URL

Finds a company's LinkedIn URL in Company URL Finder.

```
GET https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/company-query-to-linkedin-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Company URL Finder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/company-query-to-linkedin-url?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/company-query-to-linkedin-url?${params}`, {
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
| `query` | string | yes | Lookup query passed to Company URL Finder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exists": true,
      "linkedinUrl": "https://example.com",
      "remainingCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exists` | boolean | Whether a matching LinkedIn company URL was found for the submitted query. |
| `linkedinUrl` | string | LinkedIn company URL returned by Company URL Finder for the submitted query. |
| `remainingCredits` | number | Remaining Company URL Finder credits after the lookup. |

## Native endpoint

Through the native Company URL Finder API, this operation is `POST /v2/services/name_to_linkedin` (base URL `https://api.companyurlfinder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/company-query-to-linkedin-url.md) for the provider-specific parameters and requirements.

