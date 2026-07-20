# DataMerge: Get Company Hierarchy

Retrieves a company hierarchy from DataMerge by DataMerge ID.

```
GET https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-company-hierarchy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataMerge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-company-hierarchy?connectionId=$CONNECTION_ID&datamergeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datamergeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataMerge/latest/actions/get-company-hierarchy?${params}`, {
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
| `datamergeId` | string | yes |  |
| `includeBranches` | boolean | no |  |
| `includeNames` | boolean | no |  |
| `onlySubsidiaries` | boolean | no |  |
| `maxLevel` | number | no |  |
| `countryCode[]` | array<string> | no |  |
| `page` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DataMerge API returns.

## Native endpoint

Through the native DataMerge API, this operation is `GET /v1/company/hierarchy` (base URL `https://api.datamerge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-hierarchy.md) for the provider-specific parameters and requirements.

