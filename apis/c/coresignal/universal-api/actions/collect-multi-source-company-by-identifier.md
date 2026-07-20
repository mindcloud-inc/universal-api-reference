# Coresignal: Collect Multi-source Company By Identifier

Collects a multi-source company from Coresignal by identifier.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-company-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-company-by-identifier?connectionId=$CONNECTION_ID&companyIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-multi-source-company-by-identifier?${params}`, {
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
| `companyIdentifier` | string | yes |  |

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

Through the native Coresignal API, this operation is `GET /company_multi_source/collect/:companyIdentifier` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-multi-source-company-by-identifier.md) for the provider-specific parameters and requirements.

