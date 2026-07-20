# RocketReach: Lookup Company

Retrieves a company from RocketReach.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-company?${params}`, {
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
| `domain` | string | no |  |
| `id` | number | no |  |
| `linkedin_url` | string | no |  |
| `name` | string | no |  |
| `ticker` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "description": "string",
      "domain": "string",
      "email_domain": "ava@example.com",
      "funding_investors": [
        {}
      ],
      "id": 1,
      "industry": "string",
      "industry_keywords": [
        "string"
      ],
      "links": {},
      "name": "Ava Chen",
      "num_employees": 1,
      "phone": "string",
      "revenue": 1,
      "rr_profile_url": "https://example.com",
      "sic_codes": [
        1
      ],
      "website_domain": "string",
      "year_founded": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `description` | string |  |
| `domain` | string |  |
| `email_domain` | string |  |
| `funding_investors` | array<object> |  |
| `id` | number |  |
| `industry` | string |  |
| `industry_keywords` | array<string> |  |
| `links` | object |  |
| `name` | string |  |
| `num_employees` | number |  |
| `phone` | string |  |
| `revenue` | number |  |
| `rr_profile_url` | string |  |
| `sic_codes` | array<number> |  |
| `website_domain` | string |  |
| `year_founded` | string |  |

## Native endpoint

Through the native RocketReach API, this operation is `GET /company/lookup/` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-company.md) for the provider-specific parameters and requirements.

