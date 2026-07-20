# Action1: List Vulnerabilities

Retrieves vulnerabilities from Action1 for an organization.

```
GET https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-vulnerabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Action1 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-vulnerabilities?connectionId=$CONNECTION_ID&limit=25&offset=0&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/action1/latest/actions/list-vulnerabilities?${params}`, {
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
| `orgId` | string | yes | Provide an organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cisa_kev": "string",
      "cve_id": "string",
      "cvss_score": "string",
      "endpoints_count": 1,
      "organization_id": "string",
      "organization_ids": "string",
      "published_date": "string",
      "remediation_deadline": "string",
      "remediation_status": "string",
      "software": "string",
      "vector_string": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cisa_kev` | string |  |
| `cve_id` | string |  |
| `cvss_score` | string |  |
| `endpoints_count` | number |  |
| `organization_id` | string |  |
| `organization_ids` | string |  |
| `published_date` | string |  |
| `remediation_deadline` | string |  |
| `remediation_status` | string |  |
| `software` | string |  |
| `vector_string` | string |  |

## Native endpoint

Through the native Action1 API, this operation is `GET /vulnerabilities/:orgId` (base URL `https://app.action1.com/api/3.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vulnerabilities.md) for the provider-specific parameters and requirements.

