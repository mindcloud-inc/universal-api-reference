# Captain Data: Enrich People

Retrieves detailed person data from Captain Data by LinkedIn URL.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/enrich-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/enrich-people?connectionId=$CONNECTION_ID&linkedinProfileUrl=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkedinProfileUrl": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/enrich-people?${params}`, {
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
| `linkedinProfileUrl` | string | yes | LinkedIn profile URL to enrich. |
| `fullEnrich` | boolean | no | Include additional experiences, skills, and education details. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birth_date": "string",
      "company_name": "Ava Chen",
      "company_uid": "string",
      "education": [
        {}
      ],
      "experiences": [
        {}
      ],
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "headline": "string",
      "job_title": "string",
      "languages": [
        "string"
      ],
      "last_name": "Chen",
      "li_company_id": "string",
      "li_company_url": "https://example.com",
      "li_number_connections": 1,
      "li_number_followers": 1,
      "li_people_post_search_url": "https://example.com",
      "li_profile_country": "string",
      "li_profile_handle": "string",
      "li_profile_id": 1,
      "li_profile_image_url": "https://example.com",
      "li_profile_language": "string",
      "li_profile_url": "https://example.com",
      "li_school_url": "https://example.com",
      "location": "string",
      "open_to_work": true,
      "past_company_name": "Ava Chen",
      "past_company_uid": "string",
      "past_job_title": "string",
      "past_li_company_id": "string",
      "past_li_company_url": "https://example.com",
      "school_name": "Ava Chen",
      "skills": [
        {}
      ],
      "summary": "string",
      "uid": "string",
      "volunteer_experiences": [
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
| `birth_date` | string |  |
| `company_name` | string |  |
| `company_uid` | string |  |
| `education` | array<object> |  |
| `experiences` | array<object> |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `headline` | string |  |
| `job_title` | string |  |
| `languages` | array<string> |  |
| `last_name` | string |  |
| `li_company_id` | string |  |
| `li_company_url` | string |  |
| `li_number_connections` | number |  |
| `li_number_followers` | number |  |
| `li_people_post_search_url` | string |  |
| `li_profile_country` | string |  |
| `li_profile_handle` | string |  |
| `li_profile_id` | number |  |
| `li_profile_image_url` | string |  |
| `li_profile_language` | string |  |
| `li_profile_url` | string |  |
| `li_school_url` | string |  |
| `location` | string |  |
| `open_to_work` | boolean |  |
| `past_company_name` | string |  |
| `past_company_uid` | string |  |
| `past_job_title` | string |  |
| `past_li_company_id` | string |  |
| `past_li_company_url` | string |  |
| `school_name` | string |  |
| `skills` | array<object> |  |
| `summary` | string |  |
| `uid` | string |  |
| `volunteer_experiences` | array<object> |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /people/enrich` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/enrich-people.md) for the provider-specific parameters and requirements.

