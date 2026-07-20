# PredictLeads: List Similar Companies

Retrieves similar companies from the PredictLeads API.

```
GET https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-similar-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-similar-companies?connectionId=$CONNECTION_ID&companyIdOrDomain=stripe.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyIdOrDomain": "stripe.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-similar-companies?${params}`, {
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
| `companyIdOrDomain` | string | yes | Company's ID or domain. Example: `stripe.com`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `GET /companies/:company_id_or_domain/similar_companies` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-similar-companies.md) for the provider-specific parameters and requirements.

