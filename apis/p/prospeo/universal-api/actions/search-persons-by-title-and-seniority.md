# Prospeo: Search Persons by Title and Seniority

Finds persons in Prospeo by title and seniority.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-persons-by-title-and-seniority
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-persons-by-title-and-seniority?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-persons-by-title-and-seniority?${params}`, {
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
| `filters` | object | yes | Person title and seniority search filters. Default: `{"company":{"names":{"include":["Microsoft","Google","Apple"]}},"person_job_title":{"include":["CEO","CTO"],"match_only_exact_job_titles":false},"person_seniority":{"include":["C-Suite","Vice President"]}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "person": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |
| `person` | object |  |

## Native endpoint

Through the native Prospeo API, this operation is `POST /search-person` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-persons-by-title-and-seniority.md) for the provider-specific parameters and requirements.

