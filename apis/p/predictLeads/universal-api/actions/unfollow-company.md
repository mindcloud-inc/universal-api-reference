# PredictLeads: Unfollow Company

Unfollows a company in the PredictLeads API.

```
DELETE https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/unfollow-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/unfollow-company?connectionId=$CONNECTION_ID&companyIdOrDomain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyIdOrDomain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/unfollow-company?${params}`, {
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
| `companyIdOrDomain` | string | yes | Company ID or domain. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `POST /companies/:company_id_or_domain/unfollow` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unfollow-company.md) for the provider-specific parameters and requirements.

