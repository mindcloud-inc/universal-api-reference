# Coresignal: Collect Base Company By ID

Collects a base company from Coresignal by ID.

```
GET https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-company-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coresignal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-company-by-id?connectionId=$CONNECTION_ID&companyId=95737800" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "95737800"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coresignal/latest/actions/collect-base-company-by-id?${params}`, {
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
| `companyId` | number | yes | Coresignal company identifier returned by preview or bulk search results. Example: `95737800`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "canonical_url": "https://example.com",
      "employees_count": 1,
      "headquarters_country_parsed": "string",
      "id": 1,
      "industry": "string",
      "name": "Ava Chen",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canonical_url` | string |  |
| `employees_count` | number |  |
| `headquarters_country_parsed` | string |  |
| `id` | number |  |
| `industry` | string |  |
| `name` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Coresignal API, this operation is `GET /company_base/collect/:companyId` (base URL `https://api.coresignal.com/cdapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/collect-base-company-by-id.md) for the provider-specific parameters and requirements.

