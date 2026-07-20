# PredictLeads: List Company GitHub Repositories

Retrieves GitHub repositories for a PredictLeads company.

```
GET https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-company-git-hub-repositories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PredictLeads `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-company-git-hub-repositories?connectionId=$CONNECTION_ID&limit=25&offset=0&companyIdOrDomain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "companyIdOrDomain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/predictLeads/latest/actions/list-company-git-hub-repositories?${params}`, {
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
| `firstSeenAtFrom` | date | no | Only return GitHub repositories first seen after the given date (ISO 8601). |
| `firstSeenAtUntil` | date | no | Only return GitHub repositories first seen before the given date (ISO 8601). |
| `page` | number | no | Page number of shown items. Default: `1`. |
| `limit` | number | no | Limit the number of shown items per page. Default: `100`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PredictLeads API returns.

## Native endpoint

Through the native PredictLeads API, this operation is `GET /companies/:company_id_or_domain/github_repositories` (base URL `https://predictleads.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-company-git-hub-repositories.md) for the provider-specific parameters and requirements.

