# Coresignal: Collect Clean Company By Identifier

Collects a clean company from Coresignal by identifier.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-clean-company-by-identifier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-clean-company-by-identifier?connectionId=$CONNECTION_ID&companyIdentifier=it-that%25e2%2580%2599s-it" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyIdentifier": "it-that%e2%80%99s-it"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-clean-company-by-identifier?${params}`, {
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
| `companyIdentifier` | string | yes | LinkedIn company URL or shorthand name accepted by the Clean Company collect endpoint. Example: `it-that%e2%80%99s-it`. |

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

Through the native Coresignal API, this operation is `GET /company_clean/collect/:companyIdentifier` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-clean-company-by-identifier.md) for the provider-specific parameters and requirements.

