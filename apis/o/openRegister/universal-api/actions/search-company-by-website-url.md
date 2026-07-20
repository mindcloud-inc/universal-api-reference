# OpenRegister: Search Company By Website URL

Finds a company in OpenRegister by website URL.

```
GET https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/search-company-by-website-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenRegister `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/search-company-by-website-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fopenregister.de" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://openregister.de"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/search-company-by-website-url?${params}`, {
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
| `url` | string | yes | Website URL to search for. Example: `https://openregister.de`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_id": "string",
      "email": "ava@example.com",
      "phone": "string",
      "vat_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_id` | string | Matched company ID. |
| `email` | string | Email address when available. |
| `phone` | string | Phone number when available. |
| `vat_id` | string | VAT ID when available. |

## Native endpoint

Through the native OpenRegister API, this operation is `GET /v0/search/lookup` (base URL `https://api.openregister.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-company-by-website-url.md) for the provider-specific parameters and requirements.

