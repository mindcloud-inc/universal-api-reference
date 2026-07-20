# Wiza: Prospect Search

Finds the number of matching prospects in Wiza.

```
GET https://connect.mindcloud.co/v1/universal/wiza/latest/actions/prospect-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/prospect-search?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/prospect-search?${params}`, {
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
| `filters` | object | yes | Prospect search filters object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "profiles": [
          {
            "full_name": "Ava Chen",
            "job_company_name": "Ava Chen",
            "job_title": "string",
            "linkedin_url": "https://example.com",
            "location_name": "Ava Chen"
          }
        ],
        "total": 1
      },
      "status": {
        "code": 1,
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.profiles` | array<object> | Matching profiles returned by the search. |
| `data.profiles[].full_name` | string | Prospect full name. |
| `data.profiles[].job_company_name` | string | Current company name. |
| `data.profiles[].job_title` | string | Current job title. |
| `data.profiles[].linkedin_url` | string | Prospect LinkedIn URL. |
| `data.profiles[].location_name` | string | Prospect location. |
| `data.total` | number | Total number of matching profiles. |
| `status.code` | number | HTTP-style status code returned by Wiza. |
| `status.message` | string | Status message from Wiza. |

## Native endpoint

Through the native Wiza API, this operation is `POST /prospects/search` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prospect-search.md) for the provider-specific parameters and requirements.

