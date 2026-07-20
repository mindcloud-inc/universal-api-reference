# Harness: List Services

Retrieves services from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-services?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/list-services?${params}`, {
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
| `deploymentTemplateIdentifier` | string | no | Deployment template identifier filter. |
| `gitOpsEnabled` | boolean | no | Filter by GitOps enabled services. |
| `includeAllServicesAccessibleAtScope` | boolean | no | Include all accessible services at the current scope. Default: `false`. |
| `searchTerm` | string | no | Search term to include in the list response. |
| `serviceIdentifiers` | list<string> | no | Service identifiers to include. |
| `sort` | string | no | Sorting criteria for the services list. |
| `type` | string | no | Service type filter. |
| `versionLabel` | string | no | Version label filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "empty": true,
      "pageIndex": 1,
      "pageItemCount": 1,
      "pageSize": 1,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `empty` | boolean | Whether the page has no services. |
| `pageIndex` | number | Zero-based page index. |
| `pageItemCount` | number | Services returned in this page. |
| `pageSize` | number | Requested page size. |
| `totalItems` | number | Total number of services. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native Harness API, this operation is `GET /ng/api/servicesV2` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

