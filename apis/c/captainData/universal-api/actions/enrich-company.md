# Captain Data: Enrich Company

Retrieves detailed company data from Captain Data by LinkedIn URL.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/enrich-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/enrich-company?connectionId=$CONNECTION_ID&linkedinCompanyUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkedinCompanyUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/enrich-company?${params}`, {
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
| `linkedinCompanyUrl` | string | yes | LinkedIn company URL to enrich. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliates": [
        {}
      ],
      "city": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "description": "string",
      "domain": "string",
      "employees_range": "string",
      "geographic_area": "string",
      "headquarters": "string",
      "industries": [
        "string"
      ],
      "industry": "string",
      "last_funding_investors": [
        "string"
      ],
      "li_company_id": 1,
      "li_company_url": "https://example.com",
      "li_employees_url": "https://example.com",
      "li_followers_count": 1,
      "li_job_search_url": "https://example.com",
      "li_page_claimed": true,
      "location": "string",
      "locations": [
        {}
      ],
      "logo_url": "https://example.com",
      "number_employees": 1,
      "number_of_locations": 1,
      "postal_code": "string",
      "sn_company_url": "https://example.com",
      "specialties": [
        "string"
      ],
      "tagline": "string",
      "type": "string",
      "uid": "string",
      "updated_at": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliates` | array<object> |  |
| `city` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `description` | string |  |
| `domain` | string |  |
| `employees_range` | string |  |
| `geographic_area` | string |  |
| `headquarters` | string |  |
| `industries` | array<string> |  |
| `industry` | string |  |
| `last_funding_investors` | array<string> |  |
| `li_company_id` | number |  |
| `li_company_url` | string |  |
| `li_employees_url` | string |  |
| `li_followers_count` | number |  |
| `li_job_search_url` | string |  |
| `li_page_claimed` | boolean |  |
| `location` | string |  |
| `locations` | array<object> |  |
| `logo_url` | string |  |
| `number_employees` | number |  |
| `number_of_locations` | number |  |
| `postal_code` | string |  |
| `sn_company_url` | string |  |
| `specialties` | array<string> |  |
| `tagline` | string |  |
| `type` | string |  |
| `uid` | string |  |
| `updated_at` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /companies/enrich` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-company.md) for the provider-specific parameters and requirements.

