# Prospeo: Search Companies by Industry and Headcount

Finds companies in Prospeo by industry and headcount.

```
GET https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-companies-by-industry-and-headcount
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prospeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-companies-by-industry-and-headcount?connectionId=$CONNECTION_ID&filters=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filters": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prospeo/latest/actions/search-companies-by-industry-and-headcount?${params}`, {
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
| `filters` | object | yes | Company industry and headcount filters. Default: `{"company_industry":{"include":["Software Development","IT Services and IT Consulting"]},"company_headcount_range":["101-200","201-500","501-1000"]}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object |  |

## Native endpoint

Through the native Prospeo API, this operation is `POST /search-company` (base URL `https://api.prospeo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies-by-industry-and-headcount.md) for the provider-specific parameters and requirements.

