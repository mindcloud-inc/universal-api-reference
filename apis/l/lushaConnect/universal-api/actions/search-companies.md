# Lusha Connect: Search Companies

Finds companies in Lusha Connect by enrichment inputs.

```
GET https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lusha Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-companies?connectionId=$CONNECTION_ID&companies=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companies": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/search-companies?${params}`, {
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
| `companies` | list<object> | yes | List of company lookup objects. Each item must include id and may include domain, fqdn, name, or companyId. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Lusha Connect API returns.

## Native endpoint

Through the native Lusha Connect API, this operation is `POST /v2/company` (base URL `https://api.lusha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-companies.md) for the provider-specific parameters and requirements.

