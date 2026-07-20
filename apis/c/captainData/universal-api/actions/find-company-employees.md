# Captain Data: Find Company Employees

Finds company employees in Captain Data by company UID.

```
GET https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-company-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Captain Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-company-employees?connectionId=$CONNECTION_ID&companyUid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyUid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captainData/latest/actions/find-company-employees?${params}`, {
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
| `companyUid` | string | yes | Captain Data company UID from Find Company or Search Companies. |
| `query` | string | no | Optional Sales Navigator people-search query for employee filtering. |
| `cursor` | string | no | Pagination cursor from the X-Pagination-Next response header. |
| `pageSize` | number | no | Captain Data fixed employee-search page size. Leave at the documented default. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "headline": "string",
      "job_title": "string",
      "last_name": "Chen",
      "li_profile_id": 1,
      "li_profile_url": "https://example.com",
      "location": "string",
      "profile_image_url": "https://example.com",
      "recently_hired": true,
      "recently_promoted": true,
      "sn_company_id": 1,
      "summary": "string",
      "tenure_end": "string",
      "tenure_length": "string",
      "tenure_start": "string",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `headline` | string |  |
| `job_title` | string |  |
| `last_name` | string |  |
| `li_profile_id` | number |  |
| `li_profile_url` | string |  |
| `location` | string |  |
| `profile_image_url` | string |  |
| `recently_hired` | boolean |  |
| `recently_promoted` | boolean |  |
| `sn_company_id` | number |  |
| `summary` | string |  |
| `tenure_end` | string |  |
| `tenure_length` | string |  |
| `tenure_start` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Captain Data API, this operation is `GET /companies/:company_uid/employees` (base URL `https://api.captaindata.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-company-employees.md) for the provider-specific parameters and requirements.

