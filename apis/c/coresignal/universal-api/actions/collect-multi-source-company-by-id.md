# Coresignal: Collect Multi-source Company By ID

Collects a multi-source company from Coresignal by ID.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-company-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-company-by-id?connectionId=$CONNECTION_ID&companyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-company-by-id?${params}`, {
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
| `companyId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company_name": "Ava Chen",
      "employees_count": 1,
      "hq_country": "string",
      "id": 1,
      "industry": "string",
      "linkedin_url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `employees_count` | number |  |
| `hq_country` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `linkedin_url` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /company_multi_source/collect/:companyId` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-multi-source-company-by-id.md) for the provider-specific parameters and requirements.

