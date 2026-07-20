# RocketReach: Lookup Person And Company

Retrieves a person and company from RocketReach.

```
GET https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-person-and-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RocketReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-person-and-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketReach/latest/actions/lookup-person-and-company?${params}`, {
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
| `current_employer` | string | no |  |
| `email` | string | no |  |
| `id` | number | no |  |
| `linkedin_url` | string | no |  |
| `lookup_type` | string | no | Standard, premium, bulk, phone, or enrich lookup mode. |
| `name` | string | no |  |
| `npi_number` | number | no |  |
| `title` | string | no |  |
| `webhook_id` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birth_year": 1,
      "city": "string",
      "company": {},
      "country": "string",
      "country_code": "string",
      "current_employer": "string",
      "current_employer_domain": "string",
      "current_employer_id": 1,
      "current_employer_industry": "string",
      "current_employer_linkedin_url": "https://example.com",
      "current_employer_website": "string",
      "current_personal_email": "ava@example.com",
      "current_title": "string",
      "current_work_email": "ava@example.com",
      "education": [
        {}
      ],
      "emails": [
        {}
      ],
      "id": 1,
      "job_history": [
        {}
      ],
      "linkedin_url": "https://example.com",
      "links": {},
      "location": "string",
      "name": "Ava Chen",
      "phones": [
        {}
      ],
      "profile_list": {},
      "profile_pic": "string",
      "recommended_email": "ava@example.com",
      "recommended_personal_email": "ava@example.com",
      "recommended_professional_email": "ava@example.com",
      "region": "string",
      "return_cached_emails": true,
      "skills": [
        "string"
      ],
      "status": "string",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birth_year` | number |  |
| `city` | string |  |
| `company` | object |  |
| `country` | string |  |
| `country_code` | string |  |
| `current_employer` | string |  |
| `current_employer_domain` | string |  |
| `current_employer_id` | number |  |
| `current_employer_industry` | string |  |
| `current_employer_linkedin_url` | string |  |
| `current_employer_website` | string |  |
| `current_personal_email` | string |  |
| `current_title` | string |  |
| `current_work_email` | string |  |
| `education` | array<object> |  |
| `emails` | array<object> |  |
| `id` | number |  |
| `job_history` | array<object> |  |
| `linkedin_url` | string |  |
| `links` | object |  |
| `location` | string |  |
| `name` | string |  |
| `phones` | array<object> |  |
| `profile_list` | object |  |
| `profile_pic` | string |  |
| `recommended_email` | string |  |
| `recommended_personal_email` | string |  |
| `recommended_professional_email` | string |  |
| `region` | string |  |
| `return_cached_emails` | boolean |  |
| `skills` | array<string> |  |
| `status` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native RocketReach API, this operation is `GET /profile-company/lookup` (base URL `https://api.rocketreach.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-person-and-company.md) for the provider-specific parameters and requirements.

