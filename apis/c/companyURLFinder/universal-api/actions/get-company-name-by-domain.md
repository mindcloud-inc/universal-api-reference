# Company URL Finder: Get Company Name by Domain

Finds a company name in Company URL Finder by domain.

```
GET https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/get-company-name-by-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Company URL Finder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/get-company-name-by-domain?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companyURLFinder/latest/actions/get-company-name-by-domain?${params}`, {
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
| `domain` | string | yes | Company domain. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyName": "Ava Chen",
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
| `companyName` | string | Company name returned by Company URL Finder for the submitted domain. |
| `exists` | boolean | Whether a matching company name was found for the submitted domain. |
| `remainingCredits` | number | Remaining Company URL Finder credits after the lookup. |

## Native endpoint

Through the native Company URL Finder API, this operation is `POST /v2/services/domain_to_name` (base URL `https://api.companyurlfinder.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-name-by-domain.md) for the provider-specific parameters and requirements.

